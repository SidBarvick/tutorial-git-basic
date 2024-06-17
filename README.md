# Tutorial básico de versionamento de arquivos com Git
## Começando a usar o Git

## Comandos básicos

### git init (dentro da pasta raiz do repositório)
    Iniciar um novo repositório para versionamento pelo Git
### git status
    Mostra as informações do repositório e dos arquivos
### git add + nome do arquivo
    Modifica o status do arquivo para staged (adiciona um arquivo na área de stage) 
### git diff
    Mostra as diferenças dos arquivos entre os estados unmodified e modified
### git diff --staged
    Mostra as diferenças dos arquivos entre os estados modified e staged
### git commit + -m "Mensagem, geralmente o título do commit realizado ou uma breve indicação das alterações realizadas" : 
    Salva o estado atual de todos os arquivos do projeto 
### git log
    Mostra as informações de todos os registros de commit realizados
### git restore + nome do arquivo
    Desfaz as alterações do arquivo, considerando as diferenças entre os estados unmodified e modified
### git restore --staged + nome do arquivo
    Desfaz as alterações do arquivo, considerando as diferenças entre os estados modified e staged
### git remote
    visualiza a lista de repositórios remotos disponíveis
### git push + nome repositório + nome da branch
    Faz o update dos dados do projeto salvos no último commit executado
### git pull
    Faz o update e o merge dos dados salvos no repositório local com os dados salvos no repositório remoto. (Cuidado! Após enviar o comando o git faz a mesclagem das informações sem perguntar se o usuário esta de acordo ou não com as diferenças entre as versões dos arquivos)
### git fetch
    

## Nomenclaturas

Estado "Unstacked" : arquivos novos (arquivos que o git nunca versionou, ou seja, o comando "commit" ainda não foi executado nesses arquivos)
Estado "Unmodified" : arquivos não modificados
Estado "Modified" : arquivos modificados
Estado "Staged" : arquivos prontos para commit

## Conceitos

### "Commit de um projeto" 
    Quando é feito o commit em um projeto o Git salvo o estado atual do projeto, isso significa que o Git salvará na memória todos os dados dos arquivos naquele momento, como se fosse um checkpoint do projeto. Isso pode ser útil futuramente, caso seja necessário desfazer alguma alteração ou seja retornar para este estado salvo, ou para criar novas branchs.
