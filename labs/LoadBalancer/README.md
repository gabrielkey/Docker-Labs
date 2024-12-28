# Load Balancer

Este laboratório demonstra a configuração de um Load Balancer simples utilizando o Nginx em um ambiente Docker. O objetivo é distribuir o tráfego de entrada entre três servidores de backend (node1, node2 e node3) utilizando o Nginx como proxy reverso.

## O que é o Nginx?

É um software open source que possui diversas utilizações como: WebServer, Proxy Reverso, Caching, Load Balancer, Media Streaming, Proxy de Emails. [Documentação do Nginx.](https://nginx.org/en/docs/)

## O que é proxy Reverso?

Um proxy reverso é um servidor que encaminha as requisições dos clientes para um ou mais servidores backend, ocultando sua identidade e distribuindo a carga entre eles. Ao invés de o cliente se comunicar diretamente com o servidor de destino, ele interage com o proxy reverso, que decide qual servidor backend deve processar a solicitação. Essa técnica é frequentemente usada para balanceamento de carga, segurança (ocultando a infraestrutura interna) e otimização de desempenho (como cache de conteúdo).

# Iniciar laboratório

Os testes deste laboratório foram realizados em um ambiente Linux, especificamente no Ubuntu e Debian. Também utilizei a Linode para realizar os testes em uma máquina virtual (VM). **Partiremos do princípio de que o Docker já está instalado em seu sistema.**

### Clonar repositório

Clone o repositório e entre na pasta do laboratório.

```bash
git clone https://github.com/gabrielkey/Docker-Labs/ && cd ./Docker-Labs/labs/LoadBalancer
```

### Iniciar Containers

Para rodar os containers, use o docker compose. Para deixar em background, use a flag `-d`.

```bash
docker compose up -d
```

#### Observações

1. Os arquivos de configuração foram simplificados, mantendo apenas o essencial para o funcionamento do Nginx. Para adicionar suporte ao PHP, recomenda-se editar o arquivo docker-compose.yml, incluir a imagem do PHP e configurar o Nginx para direcionar as requisições para o contêiner responsável pelo PHP. Caso prefira usar o Apache em vez do Nginx, basta modificar o docker-compose.yml e substituir o Nginx pela imagem do Apache nos nodes. Consulte a [documentação do Nginx.](https://nginx.org/en/docs/) para mais informações.

2. Para simplificar o *README*, omiti diversas explicações, assumindo que você já tenha conhecimento sobre o que é o Nginx, sua configuração básica, e o funcionamento do Docker Compose.