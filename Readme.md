<h1><a id="sobre-o-projeto"> :bulb:  Sobre esta aplicação </a></h1>

Possui como objetivo na implantação de uma pipeline do projeto EyesUP, que consiste em um sistema de monitoramento de aplicações WEB e API's desenvolvido na disciplina de Desenvolvimento WEB do curso de Tecnologia de Redes de Computadores do IFPB - Campus JP. O foco aqui é na utilização de ferramentas devops para a implantação do projeto, sendo elas: Vagrant, Ansible, Docker e Docker Compose.

ps: Caso queira, também é possível estar utilizando apenas o Docker Compose para instanciar os containers e executar o projeto na sua máquina local.

<h1><a id="como-funciona"> :wrench:  Como funciona </a></h1>

A pipeline do projeto é composta por 4 etapas, sendo elas descritas abaixo pelos seus respectivos arquivos:
- `Vagrantfile`: Criação de uma máquina virtual para a implantação do projeto
- `Playbook Ansible`: Instalação e configuração de todos os softwares necessários para a execução do projeto
- `Docker Compose`: Criação de um arquivo de configuração para a execução dos containers


<h1><a id="tecnologias-utilizadas"> :rocket:  Tecnologias utilizadas</a></h1>

- [Vagrant](https://www.vagrantup.com/)
- [Ansible](https://www.ansible.com/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

<h1><a id="pre-requisitos"> :warning:  Pré-requisitos para utilizar com o Vagrantfile</a></h1>

Antes de começar, o Vagrantfile utiliza o Provider VirtualBox, portanto é necessário que o mesmo esteja instalado em sua máquina. Caso não tenha, acesse o link abaixo e siga as instruções de instalação:

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)


<h1><a id="como-rodar-o-projeto"> :computer:  Como rodar o projeto (Utilizando o Vagrantfile (VM))</a></h1>


```bash
# Clone este repositório
$ git clone https://github.com/AbranJames/EyesUp_Pipeline.git

# Acesse a pasta do projeto no terminal/cmd
$ cd EyesUp_Pipeline

# Execute o comando abaixo para criar a máquina virtual
$ vagrant up

# Nesse momento o Vagrantfile irá criar a máquina virtual e executar o playbook ansible para a instalação e configuração dos softwares necessários para a execução do projeto. Em seguida, o Docker Compose irá criar os containers e executar o projeto. Para acessar a aplicação, acesse a newtork da VM na porta 3000.
http://192.168.57.10:3000


# Para habilitar e acessar a interface gráfica do Prisma (db) da aplicação, faça o seguinte.

# i) Entre na VM com o comando abaixo
$ vagrant ssh

# ii) Veja o id do container 
$ docker container ls

# iii) Ative a interface gráfica do prisma
$ sudo docker exec -it <id do container> npx prisma studio

# v) Acesse a porta 5555. Digite no navegador:
http://192.168.57.10:5555

# Para parar a execução do projeto, execute o comando abaixo:
$ vagrant halt
```

<h1><a id="como-rodar-o-projeto"> :computer:  Como rodar o projeto (direto via container docker compose)</a></h1>


```bash
# Clone este repositório
$ git clone https://github.com/AbranJames/EyesUp_Pipeline.git

# Acesse a pasta do projeto no terminal/cmd
$ cd EyesUp_Pipeline

# Execute o comando abaixo para criar o container e executar o projeto
$ docker compose up -d

# Nesse momento o Docker Compose irá criar os containers e executar o projeto. Para acessar a aplicação, coloque no navegador:
http://localhost:3000

# Para habilitar e acessar a interface gráfica do Prisma (db) da aplicação, faça o seguinte:
$ docker container ls
$ docker exec -it <id do container> npx prisma studio

# Digite no navegador:
http://localhost:5555

# Para parar a execução do projeto, execute o comando abaixo:
$ docker compose down
```


<h1><a id="licença"> :pencil:  Licença</a></h1>


MIT License

Copyright (c) 2012-2022 Thiago Abrante de Souza

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

<h1><a id="contato"> :iphone:  Contato</a></h1>

- [Thiago A. Souza](mailto:thiago.abrante@academico.ifpb.edu.br)

