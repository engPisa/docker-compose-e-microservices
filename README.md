# Projeto de Microserviços com Docker e Nginx

Este projeto configura três microserviços isolados utilizando Docker e Nginx como servidor reverso. Cada microserviço é associado a um banco de dados PostgreSQL e é exposto em uma porta diferente. O Adminer está disponível para gerenciamento de banco de dados. A configuração também inclui o Nginx como servidor para os microserviços.

## Estrutura do Projeto

- **Microserviço 1**: Exposto na porta `8001`.
- **Microserviço 2**: Exposto na porta `8002`.
- **Microserviço 3**: Exposto na porta `8003`.
- **Adminer**: Exposto na porta `8080` para gerenciamento dos bancos de dados.

## Requisitos

- Docker
- Docker Compose

## Como Rodar o Projeto

### Passo 1: Clone o repositório

```bash
git clone <url-do-repositório>
cd <nome-do-diretório>
Passo 2: Iniciar os serviços com Docker Compose
No diretório do projeto, execute o comando:
```
```bash
Copiar
Editar
docker-compose up -d
Isso irá subir os seguintes serviços:

Três microserviços (microservice1, microservice2, microservice3), cada um com um banco de dados associado.
O Adminer, para gerenciamento dos bancos de dados.
Passo 3: Acessar os Serviços
Microserviço 1: localhost:8001
Microserviço 2: localhost:8002
Microserviço 3: localhost:8003
Adminer: localhost:8080
Passo 4: Parar os serviços
Para parar os serviços, basta rodar:
```
```bash
Copiar
Editar
docker-compose down
Estrutura de Diretórios
text
Copiar
Editar
.
├── service1/
│   └── index.html       # HTML para o microserviço 1
├── service2/
│   └── index.html       # HTML para o microserviço 2
├── service3/
│   └── index.html       # HTML para o microserviço 3
├── nginx.conf           # Arquivo de configuração do Nginx
├── docker-compose.yml   # Arquivo de configuração do Docker Compose
└── README.md            # Este arquivo
```
Configuração do Nginx
A configuração do Nginx é feita no arquivo nginx.conf, que mapeia os diretórios de cada microserviço. O Nginx estará configurado para servir os arquivos HTML de cada microserviço na URL correspondente.