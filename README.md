# Docker Labs

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?label=Licença) ![GitHub commit activity](https://img.shields.io/github/commit-activity/t/gabrielkey/Docker-Labs?label=Contribui%C3%A7%C3%B5es) ![GitHub Repo stars](https://img.shields.io/github/stars/gabrielkey/Docker-labs?style=flat&label=Estrelas)


Docker Labs é um repositório dedicado à criação de laboratórios práticos utilizando o Docker e Containers. O objetivo é aprimorar minhas habilidades com [docker](https://www.docker.com), explorando e experimentando por meio de laboratórios, enquanto continuo aprendendo sobre essa poderosa ferramenta. Este é um projeto de código aberto, e estou convidando você a contribuir e estudar junto comigo. Vamos aprender e evoluir juntos!

# O que é Docker e Containers?
### Docker

Docker é uma plataforma que facilita a criação, o envio e a execução de aplicações em containers. Containers são pacotes leves e portáteis que incluem tudo o que é necessário para executar uma aplicação, como o código, as bibliotecas, as dependências e o sistema de arquivos necessário para rodá-la. O Docker usa containers para garantir que a aplicação seja executada de maneira consistente, independentemente do ambiente em que está sendo executada (seja no seu computador, em servidores ou na nuvem).

### Containers
Um container é uma unidade de software isolada que empacota uma aplicação e todas as suas dependências de forma que ela possa ser executada de forma consistente em qualquer lugar. Diferente das máquinas virtuais, que emulam um sistema operacional completo, os containers compartilham o mesmo kernel do sistema operacional host, tornando-os mais eficientes em termos de recursos e mais rápidos para iniciar.

# Instalar Docker (Linux Ubuntu)
A instalação a seguir é destinada a distribuições baseadas no Ubuntu, incluindo o próprio Ubuntu. Se você estiver utilizando outro sistema operacional, consulte a [documentação oficial](https://docs.docker.com/engine/install/ubuntu/) do Docker para encontrar as instruções específicas. Para Windows, recomendamos o [Docker Desktop.](https://docs.docker.com/desktop/setup/install/windows-install/)

```bash
# Adicionando a chave oficial GPG do Docker. 
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Adicionando as dependencias no APT.
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

# Instalando o Docker.
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```
#### Testando o Docker
Para testar o Docker use a imagem "hello-world"!
```bash
# Testando o docker.
sudo docker run hello-world
```

## Labs

Os laboratórios estão organizados por software. Clique em cada pasta para explorar os projetos específicos destinados a cada ferramenta.

- [Wordpress]()

### Contribuidores

- [Gabrielkey](https://github.com/gabrielkey)