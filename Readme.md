<h1><a id="sobre-o-projeto"> :bulb:  Sobre esta aplicação </a></h1>

Consiste na implantação de uma pipeline do projeto EyesUP, que consiste em um sistema de monitoramento de aplicações WEB e API's desenvolvido na disciplina de Desenvolvimento WEB do curso de Tecnologia de Redes de Computadores do IFPB - Campus JP. O foco aqui é na utilização de ferramentas devops para a implantação do projeto, sendo elas: Vagrant, Ansible, Docker e Docker Compose.

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

<h1><a id="como-rodar-o-projeto"> :computer:  Como rodar o projeto</a></h1>


```bash
# Clone este repositório
$ git clone https://github.com/

# Acesse a pasta do projeto no terminal
$ cd Project_API_DW

# Instale as dependências
$ npm i

# Crie um arquivo .env na raiz do projeto e adicione as seguintes variáveis de ambiente
# JWT
$ SECRET=secret_anything

# BCRYPT
$ SALT=10

# Prisma
DATABASE_URL="file:./dev.db"

# Nodemailer
$ EMAIL=your_email
$ PASSWORD=your_password

# PS: Para o envio das notificações via email, alterar as constantes "user" "pass" no arquivo notifyController.js (linhas 9, 10 e 20) para as variáveis de ambiente EMAIL e PASSWORD

# Execute a aplicação em modo de desenvolvimento
$ npm run dev

# O servidor inciará na porta:3000 - acesse http://localhost:3000
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
















