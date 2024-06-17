## Tutorial Básico de versionamento de arquivos com Git

### Comandos básicos

>> git init (dentro da pasta raiz do repositório)
    Iniciar um novo repositório para versionamento pelo Git
>> git status
    Mostra as informações do repositório e dos arquivos
>> git add + nome do arquivo
    Modifica o status do arquivo para staged (adiciona um arquivo na área de stage) 
>> git diff
    Mostra as diferenças entre os arquivos unmodified e modified
>> git diff --staged
    Mostra as diferenças entre os arquivos staged
>> git commit + -m "Mensagem, geralmente o título do commit realizado ou uma breve indicação das alterações realizadas" : 
    Salva o estado atual do projeto 
>> git log
    Mostra todos os registros de commit realizados
>> git restore + nome do arquivo
    Desfaz as alterações do arquivo, considerando as diferenças entre os estados unmodified e modified
>> git restore --staged + nome do arquivo
    Desfaz as alterações do arquivo, considerando as diferenças entre os estados modified e staged

### Nomenclaturas

>> Unstacked : arquivos novos 
>> Unmodified : arquivos não modificados
>> Modified : arquivos modificados
>> Staged : arquivos prontos para commit

### Conceitos

>> "Commit de um projeto" 
    Quando é feito o commit em um projeto o Git salvo o estado atual do projeto, isso significa que o Git salvará na memória todos os dados dos arquivos naquele momento, como se fosse um snapshot. Isso pode ser útil futuramente, caso se necessário desfazer alguma alteração, ou para criar novas branchs.