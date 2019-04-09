### ![tittle01.png](/imagens/01.png)

Documento com os passos para instalação e configuração das ferramentas necessárias para automação de testes web utilizando o framework:

- **Ruby** (Linguagem de programação para escrita dos scripts)


- **Capybara** (Gem de emulação de browser, mais ou menos o que o selenium faz, porém de forma mais simples.


- **Cucumber** (Ferramenta para executar os testes utilizando a técnica de BDD)


- **Sublime Text** (IDE para edição dos textos de desenvolvimento)


- **CMDER** (Terminal para utilizar a linha de comando)

### ![tittle02.png](/imagens/02.png)

No processos de instalação, configuração e desenvolvimento das automações, iremos utilizar a linha de comando muitas vezes.

O CMDER entra como uma melhor alternativa para não utilizarmos o ”cmd”, a interface é mais animada e de fácil entendimento além de possuir comandos do Linux (cat, ls, rm, grep)

1. Acesse o site: https://cmder.net/ e faça o download da versão FULL (recomendada porque já tem integração com o Git).

2. Descompacte o arquivo baixado em uma pasta/diretória de sua preferência. Ex: **(C:\cmder\)**

3. Abra a pasta e execute o arquivo **cmder.exe**

**Dica:** Para facilitar, crie um atalho do arquivo **cmder.exe** na área de trabalho, isso evita ir sempre até o C: para abrir o CMDER.

![image.png](/imagens/cmder.png)

### ![tittle03.png](/imagens/03.png)

Sublime text é um editor de textos leve com suporte a plugins e vários outros recursos que auxiliam o desenvolvimento.

1. Acesse o site https://www.sublimetext.com/3 e faça o download da versão portable (que permitirá executar através de um pendrive, por exemplo) escolha conforme sua máquina (32 ou 64bits)

2. Descompacte o arquivo baixado em uma pasta de sua preferência Ex: **(C:\sublimetext\)**

3. Abra a pasta e execute o arquivo **sublime_text.exe**

**Dica:** Para facilitar, crie um atalho do arquivo sublime_text.exe na área de trabalho, isso evita ir sempre até o **C:** para abrir o **Sublime Text.**

![image.png](/imagens/sublime.png)

### ![tittle04.png](/imagens/04.png)

O package control é um gerenciador de complementos do Sublime Text.

Existem várias extensões que facilitam o processo de desenvolvimento da automação, auto-complete e melhores visualização (cores) são algumas delas.

1. Abra o Sublime Text e no menu superior clique em: **Tools > Install Package Control**

2. Para abrir o gerenciador e instalar o plugin clique em: **Preferences > Package Control**

3. No campo de texto que será exibido digite: **Install package** e tecle **Enter**

4. Em seguida, no próximo campo de texto exibido digite: **Cucumber** e clique no resultado da busca para instalar o pacote.

![image.png](/imagens/sublime_2.png)

### ![tittle05.png](/imagens/05.png)

Com a Syntax Cucumber Gherkin habilitada, a visualização dos cenários é melhorada, destacando as palavras-chave.

Entre na URL: https://pastebin.com/1jQM8PTJ copie o exemplo de BDD e cole no Sublime Text.

Em seguida clique em: 

**View > Syntax > Cucumber > Guerkin**

![image.png](/imagens/sublime_3.png)

O texto deve ficar formatado da seguinte forma:

![image.png](/imagens/sublime_4.png)

### ![tittle06.png](/imagens/06.png)

Nessa etapa vamos iniciar o setup da máquina com as configurações da linguagem de programação, framework e drivers.

- **Ruby**
- **DevKit**
- **Bundler**
- **Gems**
- **Drivers do Chrome e Firefox**

### ![tittle07.png](/imagens/07.png)

Ruby é a linguagem de programação que vamos utilizar para construir as automações web (vamos usar a versão 2.3.3)

1. Acesse a página: https://rubyinstaller.org/downloads/ e faça o download da **versão 2.3.3** de acordo com o sistema do PC **(32 ou 64 bits)**.

2. Execute o arquivo baixado, na tela de escolha do local para salvamento e opcionais **selecione as 3 opções:**

       - Install Tcl/Tk support
       - Add Ruby executables to yout PATH
       - Associate .rb and .rbw files with this Ruby Installation

![image.png](/imagens/ruby.png)

### ![tittle08.png](/imagens/07_1.png)

1. Para validar a instalação correta do Ruby, abra o **CMDER** e digite **ruby –v** 

![image.png](/imagens/ruby_2.png)

**(Caso o CMDER esteja aberto durante a instalação feche-o e refaça o step acima)**

### ![tittle09.png](/imagens/08.png)

DevKit é um pacote de ferramentas que permite fazer build e usar extensões nativas em Ruby.

1. Acesse a página: https://rubyinstaller.org/downloads/ e desça a barra de rolagem até visualizar o rodapé, o tópico com o Development Kit estará visível.

2. Faça o download do instalador compatível com a versão do Ruby e arquitetura da máquina **(Ruby 2.3.3 e 32/64 Bits)**

3. Execute o arquivo de instalação e selecione a pasta de instalação do pacote conforme essa estrutura **C:\Ruby23-x64\DevKit**\ (criar a pasta **DevKit** no Diretório do ruby **(C:\Ruby23-x64))**

Os arquivos deverão ser extraídos no diretório **C:\Ruby23-x64\DevKit**\  indicado.

![image.png](/imagens/devkit.png)

### ![tittle10.png](/imagens/09.png)

1. Agora, no CMDER, acesse a pasta onde foram extraídos os arquivos do DevKit:

    **C:\Ruby23-x64\DevKit**\

2. Dentro da pasta, execute os comandos a seguir para iniciar o script de instalação:

    r**uby dk.rb init**
    **ruby dk.rb install**

Ao concluir esses steps, o Development Kit foi instalado.

![image.png](/imagens/devkit_2.png)

### ![tittle11.png](/imagens/10.png)

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

![image.png](/imagens/ssl.png)

### ![tittle12.png](/imagens/11.png)

Bundler é o gerenciador de dependências para projetos Ruby.

Após instalar o bundler, todas as dependências do projeto declaradas no arquivo Gemfile serão baixadas.

1. Abra o CMDER e execute o comando: 
    **gem install bundler**

    _(gem install ”nome_da_gem” é o comando utilizado para se instalar gems)_

* Com o bundler instalado e o arquivo Gemfile criado, basta executar um **bundle** ou **bundle install** dentro da pasta principal do projeto para que seja feito o download de todas as gems (lib`s).

![image.png](/imagens/bundler.png)

### ![tittle13.png](/imagens/12.png)

No caso do Firefox e outros navegadores, podemos utilizar o geckodriver.

Nesse step vamos ver a instalação do Driver para o Firefox (geckodriver):

1. Acesse https://github.com/mozilla/geckodriver/releases
Procure o bloco de downloads do release mais recente e clique no link do pacote referente ao Sistema operacional e arquitetura da máquina (32 ou 64Bits).

2. Extraia o conteúdo do arquivo baixado para a pasta **C:\Ruby23-x64\bin** (pasta de instalação do Ruby)

![image.png](/imagens/geckodriver.png)

### ![image.png](/.attachments/13.png)

Na automação de testes web é necessário ferramentas para fazer ligação dos scripts de automação com o navegador, e os drivers são para este fim.

Nesse step vamos ver a instalação do Driver para o Chrome (chromedriver):

1. Acesse http://chromedriver.chromium.org/ e clique no release mais recente.

2. Na página que abriu clique em **chromedriver_win32.zip** (mesmo que sua máquina seja 64bits)

3. Extraia o conteúdo do arquivo baixado para a pasta **C:\Ruby23-x64\bin** (pasta de instalação do Ruby)

![image.png](/.attachments/chromedriver.png)




























