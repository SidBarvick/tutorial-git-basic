# Tutorial básico de versionamento de arquivos com Git por meio de linha de comando

**Sobre** : Tutorial com informações básicas e resumidas sobre como utilizar o Git por meio da linha de comando para versionamento de códigos e arquivos, destinado para pessoas que estão começando a utilizar essa ferramenta.

## Nomenclaturas e Conceitos 
#### *(Termos ordenados em uma lógica progressiva para facilitar o entendimento)*

- **Commit** <br/> Quando é feito o commit em um projeto o Git salva o estado atual do projeto, isso significa que o Git salvará na memória todos os dados dos arquivos naquele instante, como se fosse um checkpoint do projeto. Isso pode ser útil futuramente, caso seja necessário desfazer alguma alteração, bastando para tanto retornar para o estado salvo no commit (checkpoint) desejado. Os commits também são úteis para definir um ponto de referência para a criação de outras branchs, garantindo assim que as branchs tenham um ponto de referência em comum para um melhor entendimento e coerência do fluxo de desenvolvimento de um projeto. 
- **Unstacked** <br/> Estado que indica que o arquivo é novo no projeto, ou seja, um arquivo que o Git nunca versionou e não há informações de nenhum estado anterior.
- **Unmodified** <br/> Estado que indica que o arquivo não foi modificado, em comparação ao último commit realizado.
- **Modified** <br/> Estado que indica que o arquivo foi modificado, em comparação ao último commit realizado.
- **Staged** <br/> Estado que indica que o arquivo está pronto para realizar o commit. Arquivos que não estão no estado staged serão desconsiderados no próximo commit.
- **Branch** <br/> Fluxo de desenvolvimento, um projeto pode ter várias branchs que podem sofrer modificações independentes e assim gerar estados diferentes do código e dos arquivos do projeto, que posteriormente podem ser meclados ou não pelos desenvolvedores. Esse conceito é muito útil para o desenvolvimento em paralelo por pessoas diferentes.
- **Head** <br/> Seletor que indica a branch que o usuário está manipulando atualmente, ou seja, apenas a branch com o seletor "Head" poderá sofrer alterações pelo usuário.
- **.gitgnore** <br/> Arquivo utilizado para indicar o nome dos arquivos que devem ser ignorados pelo Git, ou seja, arquivos que o Git não precisa fazer o versionamento das modificações realizadas.

## Comandos básicos

- **git init** <br/> Iniciar um novo repositório para versionamento pelo Git. O comando deve ser executado dentro da pasta raiz do projeto.
- **git status** <br/> Mostra as informações do repositório e dos arquivos
- **git add + nome do arquivo** <br/> Modifica o status do arquivo para staged (adiciona um arquivo na área de stage) 
- **git diff** <br/> Mostra as diferenças dos arquivos entre os estados unmodified e modified
- **git diff --staged** <br/> Mostra as diferenças dos arquivos entre os estados modified e staged
- **git commit -m "comentário do commit"** <br/> Salva o estado atual de todos os arquivos do projeto 
- **git log** <br/> Mostra as informações de todos os registros de commit realizados
- **git restore + nome do arquivo** <br/> Desfaz as alterações do arquivo, considerando as diferenças entre os estados unmodified e modified
- **git restore --staged + nome do arquivo** <br/> Desfaz as alterações do arquivo, considerando as diferenças entre os estados modified e staged
- **git remote** <br/> Visualiza a lista de repositórios remotos disponíveis
- **git push + nome repositório remoto + nome da branch** <br/> Atualiza (update) os dados do projeto no repositório remoto, conforme o último commit executado
- **git pull + nome repositório remoto + nome da branch** <br/> Atualiza (update) e mescla (merge) os dados salvos no repositório local com os dados salvos no repositório remoto. (Cuidado! Após enviar este comando, o git faz a mesclagem das informações sem perguntar se o usuário esta de acordo ou não com as diferenças entre as versões dos arquivos)
- **git fetch** <br/> Faz o download das informações do repositório remoto sem aplicar ou mesclar as diferenças entre os repositórios, depois deste comando é possível executar o comando git diff + nome do repositório + / + nome da branch para visualizar as diferenças entre os repositórios antes de tomar a decisão de executar o comando git pull para a mesclagem (merge) das informações.
- **git branch + nome da branch** <br/> Cria um nova branch no projeto
- **git log --oneline --decorate** <br/> Mostra as informações resumidas dos registros dos commits, as branchs e a branch com a marcação "Head" que é a branch que esta sendo manipulada pelo usuário
- **git checkout + nome da branch** <br/> Altera o seletor "Head" para a branch que o usuário deseja manipular
- **git merge + nome da branch -m "comentário do merge"** <br/> Mescla as alterações da branch que o usuário está com a branch que o usuário indicou no comando. Contudo se houveram diferenças entre arquivos com o mesmo nome, o Git não vai executar o comando e pedirá que seja resolvido os conflitos antes de realizar o comando merge novamente. 

## Referências
- Git (https://git-scm.com/docs)

### Autor
*Sidney Barvick Fº*
    
