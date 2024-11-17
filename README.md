
# Lista de comandos mais usados no Linux
# Numa manutenção de rotina usa-se os comandos em momentos de monitoração e (ou) urgência:

- ls: Lista todos os arquivos do diretório
- df: Mostra a quantidade de espaço usada no disco rígido
- top: Mostra o uso da memória
- cd: Acessa uma determinada pasta (diretório)
- mkdir: Cria um diretório
- rm: Remove um arquivo/diretório
- cat: Abre um arquivo
- vi: Abre o editor vi (lê-se viai) para editar/criar arquivos

# Comandos de Edição de Texto
- emacs: Editor de texto screen-oriented
- pico: Editor de texto screen-oriented, também chamado de nano
- sed: Editor de texto stream-oriented
- vi: Editor de texto full-screen
- vim: Editor de texto full-screen melhorado (vi improved)

# Comandos de Gestão de Arquivos e Diretórios
- cd: Mudar de diretório atual, como por exemplo cd diretório, cd .., cd /
- chmod: Mudar a proteção de um arquivo ou diretório, como por exemplo chmod 777, parecido com o attrib do MS-DOS
- chown: Mudar o dono ou grupo de um arquivo ou diretório, vem de change owner
- chgrp: Mudar o grupo de um arquivo ou diretório
- cmp: Compara dois arquivos
- comm: Seleciona ou rejeita linhas comuns a dois arquivos selecionados
- cp: Copia arquivos, como o copy do MS-DOS
- crypt: Encripta ou Descripta arquivos (apenas CCWF)
- diff: Compara o conteúdo de dois arquivos ASCII
- file: Determina o tipo de arquivo
- grep: Procura um arquivo por um padrão, sendo um filtro muito útil e usado, por exemplo um cat a.txt | grep ola irá mostrar-nos apenas as linhas do arquivo a.txt que contenham a palavra “ola”
- gzip: Comprime ou expande arquivo
- ln: Cria um link a um arquivo
- ls: Lista o conteúdo de uma diretório, semelhante ao comando dir no MS-DOS
- lsof: Lista os arquivos abertos, vem de list open files
- mkdir: Cria uma diretório, vem de make directory”
- mv: Move ou renomeia arquivos ou diretórios
- pwd: Mostra-nos o caminho por inteiro da diretório em que nos encontramos em dado momento, ou seja um pathname
- quota: Mostra-nos o uso do disco e os limites
- rm: Apaga arquivos, vem de remove, e é semelhante ao comando del no MS-DOS, é preciso ter cuidado com o comando rm * pois apaga tudo sem confirmação por defeito
- rmdir: Apaga diretório, vem de remove directory
- stat: Mostra o estado de um arquivo, útil para saber por exemplo a hora e data do último acesso ao mesmo
- sync: Faz um flush aos buffers do sistema de arquivos, sincroniza os dados no disco com a - - memória, ou seja escreve todos os dados presentes nos buffers da memória para o disco
- sort: Ordena, une ou compara texto, podendo ser usado para extrair informações dos arquivos de texto ou mesmo para ordenar dados de outros comandos como por exemplo listar arquivos - ordenados pelo nome
- tar: Cria ou extrai arquivos, muito usado como programa de backup ou compressão de arquivos
- tee: Copia o input para um standard output e outros arquivos
- tr: Traduz caracteres
- umask: Muda as proteções de arquivos
- uncompress: Restaura um arquivo comprimido
- uniq: Reporta ou apaga linhas repetidas num arquivo
- wc: Conta linhas, palavras e mesmo caracteres num arquivo

#  Mais comandos:

- cd - change directory
- "." - diretório atual
- ".." - diretório acima
- "/"- o diretório root ou a separação de diretórios
- "~" - home (cd sem nada vai para a home)
- "-" menos - volta para o diretório que anterior
- tree - mostra a árvore do diretório atual
- -d - diretórios
- -a - mostra arquivos ocultos
- cat - concatena e/ou mostra o conteúdo de um arquivo
- -n - enumera as linhas
- tail - lista as últimas linhas do arquivo
- -NÚMERO - mostra a quantidade de linhas que for adicionado em NÚMERO.
- -f - continua assistindo o arquivo em busca de novos dados.
- wc - conta linhas, palavras e caracteres
- -l - linhas
- -m - caracteres
- -w - palavras

# Alguns símbolos e operadores úteis
- ; - permite executar vários comandos na mesma linha. Roda todos os comandos, mesmo se ocorrer algum erro.
- && - permite executar vários comandos na mesma linha. Se o comando anterior não gerar nenhum erro, continua a corrente de comandos, do contrário, para no momento que ocorrer um erro.
- || - permite executar vários comandos na mesma linha. Ele funciona de maneira oposta ao anterior, ou seja, se ocorrer algum erro no comando anterior, executa o próximo comando, do contrário, para no primeiro comando que NÃO gerar um erro.
- | - Joga a saída (output) de um comando para a entrada (input) de outro.
- > - Joga a saída de um comando e redireciona para um arquivo. Apaga o arquivo todo e substitui seu conteúdo.
- >> - Joga a saída de um comando e redireciona para um arquivo. Não apaga o que estiver no arquivo, apenas adiciona o novo conteúdo na última linha.
- & - Joga para o background. Veja jobs e fg para complementar
# Background e Foreground
- jobs - mostra trabalhos em execução
- fg %n - leva o que estiver em background para o foreground
- bg %n - continua um job em background
- kill %n - mata um job
# Outros comandos
- nano - editor de textos
- file - mostra o tipo do arquivo
- history - histórico de comandos já digitados
- pkill - mata processos
- whoami - mostra seu usuário
- hostname - mostra o nome do seu computador
- uname - mostra dados sobre o sistema
- ps aux - mostra todos os processos rodando no sistema no momento da execução
