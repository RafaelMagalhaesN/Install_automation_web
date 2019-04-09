### ![image.png](/imagens/01.png)

Documento com os passos para instalação e configuração das ferramentas necessárias para automação de testes web utilizando o framework:

- **Ruby** (Linguagem de programação para escrita dos scripts)


- **Capybara** (Gem de emulação de browser, mais ou menos o que o selenium faz, porém de forma mais simples.


- **Cucumber** (Ferramenta para executar os testes utilizando a técnica de BDD)


- **Sublime Text** (IDE para edição dos textos de desenvolvimento)


- **CMDER** (Terminal para utilizar a linha de comando)

### ![image.png](/.attachments/02.png)

No processos de instalação, configuração e desenvolvimento das automações, iremos utilizar a linha de comando muitas vezes.

O CMDER entra como uma melhor alternativa para não utilizarmos o ”cmd”, a interface é mais animada e de fácil entendimento além de possuir comandos do Linux (cat, ls, rm, grep)

1. Acesse o site: https://cmder.net/ e faça o download da versão FULL (recomendada porque já tem integração com o Git).

2. Descompacte o arquivo baixado em uma pasta/diretória de sua preferência. Ex: **(C:\cmder\)**

3. Abra a pasta e execute o arquivo **cmder.exe**

**Dica:** Para facilitar, crie um atalho do arquivo **cmder.exe** na área de trabalho, isso evita ir sempre até o C: para abrir o CMDER.

![image.png](/imagens/cmder.png)

### ![image.png](/.attachments/image-b515fa3b-d0f3-443d-961e-1fa9ff659b9d.png)

Sublime text é um editor de textos leve com suporte a plugins e vários outros recursos que auxiliam o desenvolvimento.

1. Acesse o site https://www.sublimetext.com/3 e faça o download da versão portable (que permitirá executar através de um pendrive, por exemplo) escolha conforme sua máquina (32 ou 64bits)

2. Descompacte o arquivo baixado em uma pasta de sua preferência Ex: **(C:\sublimetext\)**

3. Abra a pasta e execute o arquivo **sublime_text.exe**

**Dica:** Para facilitar, crie um atalho do arquivo sublime_text.exe na área de trabalho, isso evita ir sempre até o **C:** para abrir o **Sublime Text.**

![image.png](/.attachments/image-cc6f9f06-4910-4a76-a12a-2ce4eae8102d.png)

### ![image.png](/.attachments/image-067ac147-25c1-4543-887b-5f23e8584b4c.png)

O package control é um gerenciador de complementos do Sublime Text.

Existem várias extensões que facilitam o processo de desenvolvimento da automação, auto-complete e melhores visualização (cores) são algumas delas.

1. Abra o Sublime Text e no menu superior clique em: **Tools > Install Package Control**

2. Para abrir o gerenciador e instalar o plugin clique em: **Preferences > Package Control**

3. No campo de texto que será exibido digite: **Install package** e tecle **Enter**

4. Em seguida, no próximo campo de texto exibido digite: **Cucumber** e clique no resultado da busca para instalar o pacote.

![image.png](/.attachments/image-00f9cc75-7494-4471-91b6-c584a754f766.png)

### ![image.png](/.attachments/image-05457dd8-01af-4e05-b6ee-6e29baabf246.png)

Com a Syntax Cucumber Gherkin habilitada, a visualização dos cenários é melhorada, destacando as palavras-chave.

Entre na URL: https://pastebin.com/1jQM8PTJ copie o exemplo de BDD e cole no Sublime Text.

Em seguida clique em: 

**View > Syntax > Cucumber > Guerkin**

![image.png](/.attachments/image-c3573f45-9caa-45dc-b740-431c694feeca.png)

O texto deve ficar formatado da seguinte forma:

![image.png](/.attachments/image-8c80e730-8f30-475d-997f-8e64c45844d0.png)

### ![image.png](/.attachments/image-ca8a78f0-5bae-4c1c-b5c6-99b16302dd9d.png)

Nessa etapa vamos iniciar o setup da máquina com as configurações da linguagem de programação, framework e drivers.

- **Ruby**
- **DevKit**
- **Bundler**
- **Gems**
- **Drivers do Chrome e Firefox**

### ![image.png](/.attachments/image-b4097f77-76f9-49a3-a0a4-bc8410e62381.png)

Ruby é a linguagem de programação que vamos utilizar para construir as automações web (vamos usar a versão 2.3.3)

1. Acesse a página: https://rubyinstaller.org/downloads/ e faça o download da **versão 2.3.3** de acordo com o sistema do PC **(32 ou 64 bits)**.

2. Execute o arquivo baixado, na tela de escolha do local para salvamento e opcionais **selecione as 3 opções:**

       - Install Tcl/Tk support
       - Add Ruby executables to yout PATH
       - Associate .rb and .rbw files with this Ruby Installation

![image.png](/.attachments/image-74d062f1-b2df-4296-bf9f-473727f83197.png)

### ![image.png](/.attachments/image-e0ef5d24-f066-48bd-b2f7-dc1379c3fa6e.png)

1. Para validar a instalação correta do Ruby, abra o **CMDER** e digite **ruby –v** 

![image.png](/.attachments/image-4972bb15-a838-47a7-af72-82f9216b677d.png)

**(Caso o CMDER esteja aberto durante a instalação feche-o e refaça o step acima)**

### ![image.png](/.attachments/image-20a4fbd2-9115-4127-b79c-5cddf5108989.png)

DevKit é um pacote de ferramentas que permite fazer build e usar extensões nativas em Ruby.

1. Acesse a página: https://rubyinstaller.org/downloads/ e desça a barra de rolagem até visualizar o rodapé, o tópico com o Development Kit estará visível.

2. Faça o download do instalador compatível com a versão do Ruby e arquitetura da máquina **(Ruby 2.3.3 e 32/64 Bits)**

3. Execute o arquivo de instalação e selecione a pasta de instalação do pacote conforme essa estrutura **C:\Ruby23-x64\DevKit**\ (criar a pasta **DevKit** no Diretório do ruby **(C:\Ruby23-x64))**

Os arquivos deverão ser extraídos no diretório **C:\Ruby23-x64\DevKit**\  indicado.

![image.png](/.attachments/image-93339a19-3765-4107-9ae8-437fdaf69d76.png)

### ![image.png](/.attachments/image-6405988d-22c3-40a4-9c4e-d29b78aad58a.png)

1. Agora, no CMDER, acesse a pasta onde foram extraídos os arquivos do DevKit:

    **C:\Ruby23-x64\DevKit**\

2. Dentro da pasta, execute os comandos a seguir para iniciar o script de instalação:

    r**uby dk.rb init**
    **ruby dk.rb install**

Ao concluir esses steps, o Development Kit foi instalado.

![image.png](/.attachments/image-cf9de658-bf1b-4e8d-8b04-f4d62c0fdc2b.png)

### ![image.png](/.attachments/image-d307f819-9fe7-4202-bbac-cb94d6e5bc4b.png)

É possível que ocorra problemas no download das gems do Ruby devido uma falha no certificado SSL, visto que o repositório padrão é uma URL HTTPS.

Para evitar esse tipo de problema, é possível alterar o repositório para uma URL HTTP:

1. Abra o CMDER e adicione o repositório HTTP
    **gem sources –a** http://rubygems.org/

2. Remova o repositório HTTPS
    **gem sources –r** https://rubygems.org/

3. Atualize a lista de repositórios
    **gem sources –u**

4. Para validar os procedimentos, visualize a listagem de repositórios
    **gem sources –l**

![image.png](/.attachments/image-203514d5-b2bb-4b69-a633-e317b888a50b.png)

### ![image.png](/.attachments/image-64a58c38-cb34-45a2-a322-3a5fe6466e90.png)

Bundler é o gerenciador de dependências para projetos Ruby.

Após instalar o bundler, todas as dependências do projeto declaradas no arquivo Gemfile serão baixadas.

1. Abra o CMDER e execute o comando: 
    **gem install bundler**

    _(gem install ”nome_da_gem” é o comando utilizado para se instalar gems)_

* Com o bundler instalado e o arquivo Gemfile criado, basta executar um **bundle** ou **bundle install** dentro da pasta principal do projeto para que seja feito o download de todas as gems (lib`s).

![image.png](/.attachments/image-e812530d-daf1-4bdb-9bd1-c9d9d83773a4.png)

### ![image.png](/.attachments/image-ea4702c1-d129-402d-a153-f7635c6fc3f0.png)

No caso do Firefox e outros navegadores, podemos utilizar o geckodriver.

Nesse step vamos ver a instalação do Driver para o Firefox (geckodriver):

1. Acesse https://github.com/mozilla/geckodriver/releases
Procure o bloco de downloads do release mais recente e clique no link do pacote referente ao Sistema operacional e arquitetura da máquina (32 ou 64Bits).

2. Extraia o conteúdo do arquivo baixado para a pasta **C:\Ruby23-x64\bin** (pasta de instalação do Ruby)

![image.png](/.attachments/image-e0085bc6-5176-4d33-8187-eda7c3f07569.png)


























