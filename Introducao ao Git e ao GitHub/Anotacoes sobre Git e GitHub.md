# Anotações sobre Git e GitHub

Linux e sistema operacional da Apple são derivados do Unix.

Terminal do Windows é derivado do Shell e terminal do Linux é derivado do Bash. Windows 10 tem Windows Subsystem for Linux (que é um sistema Linux rodando dentro do Windows).

O Git Bash é um terminal estendido para otimizar o uso do Git, então utiliza os mesmos comandos do Unix.

SHA1 é um algoritmo de encriptação. Conjunto de caracteres de 40 dígitos é único e é uma identificação. O Git roda o sha1 não só para arquivos mas também para objetos internos do Git.

**Git é um sistema distribuído e seguro**.



### Objetos internos do GIT 

Três objetos básicos do GIT responsáveis pelo versionamento do nosso código.

- **Blobs:**
  - Os arquivos ficam guardados dentro do objeto Blob, que contém metadados dentro dele
  - Objeto blob contêm tipo de objeto (blob), tamanho da string, \0 e o conteúdo do arquivo (seja texto, binário, etc)
- **Trees:**
  - Trees armazenam blobs 
  - Crescente: blob sendo o bloco básico de composição, a tree armazenando e apontando para tipos diferentes de blobs
  - A tree também contém metadados: contém o \0, aponta para um blob, que por sua vez tem um sha1 e a tree também guarda o nome desse arquivo (ao contrário do blob, que não guarda o nome do arquivo, ele só guarda o sha do arquivo, que são os caracteres identificador dele)
  - A tree é responsável por montar a estrutura de onde estão localizados esses arquivos
  - As árvores podem apontar tanto para blobs (que são “arquivos”) ou para outras árvores - do mesmo jeito que diretórios dentro de um sistema operacional podem conter outros diretórios - faz sentido que o git use um tipo de objeto recursivo
  - As trees tem um sha1 desse metadado - as blobs tem o sha1 do arquivo, as árvores apontam para essa blob e tem um sha1 encriptado ali, os metadados das árvores.
    - Ou seja, se mudar algo no arquivo em que a tree está apontando, o sha1 do blob vai ter mudado, o que vai mudar o sha1 da tree.
- **Commits**
  - Commit é o objeto que vai juntar tudo, que vai dar sentido para a alteração que você está fazendo
  - Commit aponta para uma tree, um parente (o último commit realizado antes dele), autor e mensagem (autor e mensagem faz parte dessa ideia de sentido) e um timestamp. Significa uma alteração então a mensagem explica isso.
  - Commit também possui sha1, encriptação