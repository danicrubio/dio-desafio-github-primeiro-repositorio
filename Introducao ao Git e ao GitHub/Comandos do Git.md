# Comandos do Git

**Comandos no terminal** 

- dir (windows) ou ls (unix): lista todas os diretórios que tem na pasta em que a gente está situado
- cd (change directory): possibilita navegação entre as pastas
  - “cd /” leva pra base do diretório C
  - “cd Windows” leva a pasta Windows, por exemplos
  - “cd ..” retrocede um nível na navegação; exemplo: de C:\Windows volta para C:\
- cls (windows, clear screen) ou clear (linux, ou clicar ctrl + L): limpar a tela do terminal
- tecla tab tem função de autocompletar no windows
- mkdir (make directory): cria pasta
- echo: printa de volta no terminal um texto que você passa
  - “echo hello”: printa “hello” no terminal
  - “echo hello > hello.txt” checa se existe um arquivo hello.txt na pasta e se não houver, cria um escrito hello. 
    - símbolo “>” é um redirecionador de fluxo, então ele vai pegar o output da função echo, a saída da função echo, e jogar em um arquivo
- del (windows): deleta apenas arquivos dentro das pastas
- tecla setinha pra cima pra ver os comandos que foram utilizados anteriormente
- rmdir /S /Q (remove directory, windows): deleta os repositórios/pastas com os arquivos dentro
  - rmdir pasta /S /Q (/S /Q são flags)
- rm -rf (linux): apaga diretórios; -rf (recursive force) recursive significa que deleta todas as pastas dentro dessa pasta e force é para não aparecer nenhum tipo de confirmação para perguntar se você quer deletar ou não a pasta
  - rm -rf pasta/ (-rf são flags)



**Outros comandos no Git Bash**

- openssl sha1 nome: passar arquivo para algoritmo de encriptação sha1
- git hash-object --stdin: “git hash-object” espera receber um arquivo; a flag “--stdin” diz que estamos enviando um texto
  - Gera algoritmos (outro tipo de chave, outro conjunto de caracteres) diferentes se usar git ou não usar (usar openssl no caso) por causa dos blobs.
  - Tem que usar o blob para passar os metadados para a string se não usar o git e for usar o openssl sha1 - exemplo: blob 9\0conteudo (9 é o tamanho da string e tem que pôr o \0)
- ssh-keygen -t ed25519 -C nome@e/mail.com: gerar chave ssh
- cat id_ed25519.pub: comando especial para visualizar a chave pública
- eval $(ssh-agent -s): inicializar um agente para lidar com a chave privada
- ssh-add id_ed25519: passando para o agente a chave privada
- git clone nome do repositório: clonar repositório
- git init: inicia repositório do git dentro do diretório/pasta
- git add: move arquivos e dá início ao versionamento
  - git add *: * pega tudo o que foi modificado e adiciona para o staged para poder commitar
  - git add . 
  - git add -A
- git commit -m “comentario”: cria commit
- ls -a: flag “-a” permite ver pastas ocultas (.git; o . quer dizer que é uma pasta oculta)
- git-config
  - git-config --global user.email “nome@e/mail.com”: configura o email do autor do git; flag “--global” é para ser uma configuração global)
  - git-config --global user.name Nome: configura o nome do autor do git
  - git config --list
  - git config --global --unset (atributo)
- **git remote add origin link**
- git remote -v: lista as listas de repositórios remotos que tem cadastrados
- **git push origin master** (versão que eu conhecia :git push -u origin main)
- **git pull origin master**
- git status: diz se o arquivo está unmodified, modified, staged
- mv: mover para um diretório (ex: mv torta.md ./receitas/)