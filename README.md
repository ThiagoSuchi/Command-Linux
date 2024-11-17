1. comando ls
O comando ls lista o conteúdo de uma pasta, incluindo arquivos e diretórios. Aqui está a sintaxe:

ls [opções] [diretório_ou_caminho]
Se você omitir o caminho, o comando ls verificará o conteúdo do seu diretório atual. Para listar itens dentro de subpastas, adicione a opção -R . Enquanto isso, use -a para mostrar conteúdo oculto.

2. comando pwd
Para verificar o caminho completo do seu diretório de trabalho atual, use o comando pwd . Sua sintaxe é a seguinte:

pwd [opções]
O comando pwd tem apenas duas opções. A opção -L imprime o conteúdo da variável de ambiente , como atalhos, em vez do caminho real do seu local atual. Enquanto isso, -P imprime o local exato.

Por exemplo, /shortcut/folder é um atalho para /actual/path , e você está atualmente em /actual/path/dir . Se você usar a opção -L , a saída será:

/atalho/pasta/diretório
Enquanto isso, a opção -P imprimirá o caminho canônico exato:

/caminho/real/dir
3. comando cd
Use cd para navegar entre diretórios no seu Linux VPS. Ele não tem nenhuma opção, e a sintaxe é simples:

cd [caminho_ou_diretório]
Dependendo da sua localização, você pode precisar especificar apenas o diretório pai. Por exemplo, omita path de path/to/directory se você já estiver dentro de um. O comando cd tem vários atalhos:

cd – retorna ao diretório inicial do usuário atual.
cd .. – move um diretório para cima.
cd – – retorna ao diretório anterior.
4. comando mkdir
O comando mkdir permite que você crie um ou vários diretórios. A sintaxe se parece com isso:

mkdir [opções] nome_do_diretório1 nome_do_diretório2
Para criar uma pasta em outro local, especifique o caminho completo. Caso contrário, este comando criará o novo item em seu diretório de trabalho atual.

Por exemplo, digite o seguinte para criar new_folder em /path/to/target_folder :

mkdir caminho/para/pasta_de_destino/nova_pasta
Por padrão, mkdir permite que o usuário atual leia, grave e execute arquivos na nova pasta. Você pode definir privilégios personalizados durante a criação adicionando a opção -m . Para saber mais sobre gerenciamento de permissões, leia a seção chmod abaixo.

5. comando rmdir
Execute rmdir para excluir diretórios vazios no seu sistema Linux . A sintaxe do comando se parece com isso:

rmdir [opções] nome_do_diretório
O comando rmdir não funcionará se o diretório contiver subpastas. Para forçar a exclusão, adicione a opção – p . Note que você deve ser o dono do item que deseja remover ou usar sudo em vez disso.

6. comando rm
O comando rm exclui arquivos de um diretório. Você deve ter permissão de gravação para a pasta ou usar sudo . Aqui está a sintaxe:

rm [opções] arquivo1 arquivo2
Você pode adicionar a opção -r para remover uma pasta e seu conteúdo, incluindo subdiretórios. Use o sinalizador -i para exibir uma mensagem de confirmação antes da remoção ou -f para desativá-la completamente.

Aviso! Evite usar -r e -f a menos que seja necessário. Em vez disso, adicione a opção -i para evitar exclusão acidental.

7. comando cp
Use o comando cp para copiar arquivos do seu diretório atual para outra pasta. A sintaxe se parece com isso:

cp arquivo1 arquivo2 [caminho_de_destino]
Você também pode usar cp para duplicar o conteúdo de um arquivo para outro usando esta sintaxe. Se o alvo estiver em outro local, especifique o caminho completo assim:

cp source_file /caminho/para/arquivo_de_destino
Além disso, o cp permite que você duplique um diretório e seu conteúdo para outra pasta usando a opção -R :

cp -R /caminho/para/pasta /caminho/de/destino/para/pasta_copia
8. comando mv
O uso principal do comando mv é mover um arquivo ou pasta para outro local. Aqui está a sintaxe:

mv arquivo_ou_diretório [diretório_de_destino]
Por exemplo, moveremos file1.txt de outro local para o caminho /new/file/directory usando este comando:

mv /original/path/file1.txt o/caminho/de/destino
Você também pode usar o comando mv para renomear arquivos no seu sistema Linux . Aqui está um exemplo:

mv nome_antigo.txt nome_novo.txt
Se você especificar o caminho completo, poderá renomear arquivos simultaneamente e movê-los para um novo local, como neste exemplo:

mv antigo/localização/de/nome_antigo.txt novo/caminho/para/nome_novo.txt
9. comando de toque
Execute o comando touch para criar um novo arquivo vazio em um diretório específico. A sintaxe é a seguinte:

toque [opções] [caminho_e_nome_do_arquivo]
Se você omitir o caminho, o comando touch criará um novo arquivo no seu diretório de trabalho atual. Aqui está um exemplo:

arquivo touch.txt
10. comando de arquivo
O comando file verifica um tipo de arquivo, como TXT, PDF ou outro. A sintaxe é a seguinte:

arquivo [nome_do_arquivo]
Se você usar esse comando em um link simbólico , ele produzirá o arquivo real conectado ao atalho. Você pode adicionar a opção -k para imprimir informações mais detalhadas sobre o item.

O comando File mostra o arquivo real de um link simbólico
11. Comandos zip e unzip
O comando zip compacta um ou vários arquivos em um arquivo ZIP , reduzindo seu tamanho. Aqui está a sintaxe:

zip [opções] nome_do_arquivo_zip arquivo1 arquivo2
Para extrair um arquivo compactado para seu diretório de trabalho atual, use o comando unzip assim:

descompactar [opções] nome_do_arquivo_zip
12. comando tar
O comando tar agrupa vários arquivos ou diretórios em um arquivo sem compressão. A sintaxe é a seguinte:

tar [opções] tar_file_name arquivo1 arquivo2
Para criar um novo arquivo TAR , você deve adicionar a opção -c . Então, use o sinalizador -f para especificar o nome do arquivo.

Se você quiser habilitar a compactação, adicione uma opção específica com base no seu método preferido. Por exemplo, o seguinte irá agrupar file1.txt e file2.txt com a compactação gzip :

tar -cfz arquivo.tar.gz fle1.txt arquivo2.txt
Lembre-se de que o formato do arquivo do arquivo será diferente dependendo do método de compressão. Independentemente da extensão, você pode descompactar um arquivo TAR usando esta sintaxe:

tar [opções] nome_do_arquivo_tar
13. Comando nano, vi e jed
Os comandos nano , vi e jed permitem que você edite arquivos. Eles têm a mesma sintaxe, exceto no começo, onde você especifica o nome da ferramenta:

nano/vi/jed nome_do_arquivo
Se o arquivo de destino não existir, esses comandos criarão um novo. Como seu sistema pode não ter esses utilitários de processamento de texto pré-instalados, configure-os usando seu gerenciador de pacotes.

Explicaremos o comando na seção de comandos apt e dnf .

14. comando do gato
O comando concatenate ou cat tem vários usos. O mais básico é imprimir o conteúdo de um arquivo. Aqui está a sintaxe:

gato nome_do_arquivo
Para imprimir o conteúdo em ordem reversa, use tac em vez disso. Se você adicionar o símbolo do operador de saída padrão ( > ), o comando cat criará um novo arquivo. Por exemplo, o seguinte criará file.txt :

gato > arquivo.txt
Você também pode usar cat com o operador para combinar o conteúdo de vários arquivos em um novo item. Neste comando, file1.txt e file2.txt serão mesclados em target.txt :

gato arquivo1.txt arquivo2.txt > alvo.txt
15. comando grep
A expressão regular global print ou grep permite que você pesquise linhas específicas de um arquivo usando palavras-chave. É útil para filtrar dados grandes como logs. A sintaxe se parece com a seguinte:

grep [opções] palavra-chave [arquivo]
Você também pode filtrar dados de outro utilitário canalizando-os para o comando grep . Por exemplo, o seguinte pesquisa file.txt a partir da saída do comando ls :

ls | grep "arquivo.txt"
O comando grep filtra a saída do ls
16. comando sed
Use o comando sed para pesquisar e substituir padrões em arquivos rapidamente. A sintaxe básica se parece com isso:

sed [opções] 'subcomando/novo_padrão/padrão_alvo' arquivo_de_entrada
Você pode substituir uma string em vários arquivos simultaneamente listando-os. Aqui está um exemplo de um comando sed que muda vermelho em colors.txt e hue.txt para azul :

sed 's/vermelho/azul' cores.txt matiz.txt
17. comando principal
Use o comando head para imprimir as primeiras entradas de um arquivo. A sintaxe básica é a seguinte:

cabeça [opções] nome_do_arquivo
Você também pode imprimir as primeiras linhas da saída de outro comando canalizando-o assim:

comando | head [opções]
Por padrão, o head mostrará as dez primeiras linhas . No entanto, você pode alterar essa configuração usando a opção -n seguida do número desejado.

Enquanto isso, use -c para imprimir as primeiras entradas com base no tamanho do byte em vez da linha.

18. comando tail
O comando tail é o oposto de head , permitindo que você imprima as últimas linhas de arquivos ou da saída de outro utilitário. Aqui estão as sintaxes:

tail [opções] nome_do_arquivo
comando | tail [opções]
O utilitário tail também tem a mesma opção que head . Por exemplo, extrairemos as últimas cinco linhas da saída do comando ping :

ping -c 10 8.8.8.8 | cauda -n 5
O comando Tail imprime as últimas cinco linhas do ping
19. comando awk
O comando awk pesquisa e manipula padrões de expressões regulares em um arquivo. Aqui está a sintaxe básica:

awk '/padrão regex/{ação}' arquivo_de_entrada.txt
Embora similar ao sed , o awk oferece mais operações além da substituição, incluindo impressão, cálculo matemático e exclusão. Ele também permite que você execute uma tarefa complexa com uma instrução if .

Você pode executar várias ações listando-as de acordo com sua ordem de execução, separadas por ponto e vírgula ( ; ). Por exemplo, este comando awk calcula a pontuação média dos alunos e imprime nomes que estão acima desse limite:

awk -F':' '{ total += $2; alunos[$1] = $2 } FIM { média = total / comprimento(alunos); imprimir "Média:", média; imprimir "Acima da média:"; para (aluno em alunos) se (alunos[aluno] > média) imprimir aluno }' pontuação.txt
awk imprime pontuação média e alunos com pontuação acima da média
Precisa de ajuda com um comando?
Peça ao Kodee , assistente de IA da Hostinger, para detalhar e explicar comandos complexos.

20. comando sort
Use o comando sort para reorganizar o conteúdo de um arquivo em uma ordem específica. Sua sintaxe se parece com o seguinte:

classificar [opções] [nome_do_arquivo]
Observe que este utilitário não modifica o arquivo real e apenas imprime o conteúdo reorganizado como saída.

Por padrão, o comando sort usa a ordem alfabética de A a Z , mas você pode adicionar a opção -r para inverter a ordem. Você também pode classificar arquivos numericamente usando o sinalizador -n .

21. comando de corte
O comando cut seleciona seções específicas de um arquivo e as imprime como uma saída do Terminal. A sintaxe se parece com isso:

arquivo de opções de corte
Diferentemente de outros utilitários Linux, as opções do comando cut são obrigatórias para seccionamento de arquivos. Aqui estão algumas das flags:

-f – seleciona um campo de linha específico.
-b – corta a linha por um tamanho de byte especificado.
-c – secciona a linha usando um caractere especificado.
-d – separa linhas com base em delimitadores.
Você pode combinar várias opções para uma saída mais específica. Por exemplo, este comando extrai o terceiro ao quinto campo de uma lista separada por vírgulas:

cortar -d',' -f3-5 lista.txt
O comando cut extrai seções de uma lista separada por vírgulas
22. comando diff
O comando diff compara dois arquivos e imprime suas diferenças. Aqui está a sintaxe:

diff nome_do_arquivo1 nome_do_arquivo2
Por padrão, o comando diff mostra apenas as diferenças entre os dois arquivos. Para imprimir todo o conteúdo e destacar as discrepâncias, habilite o formato de contexto usando a opção -c . Você também pode ignorar a diferenciação entre maiúsculas e minúsculas adicionando -i .

Por exemplo, execute o seguinte para mostrar apenas as diferenças entre 1.txt e 2.txt :

diff -c 1.txt 2.txt
O comando diff mostra as diferenças entre os arquivos no formato de contexto
23. comando tee
O comando tee emite os resultados de outro comando para o Terminal e um arquivo. É útil se você quiser usar os dados para processamento posterior ou backups. Aqui está a sintaxe:

comando | tee [opções] nome_do_arquivo
Se o arquivo especificado não existir, tee o criará. Tenha cuidado ao usar este comando, pois ele sobrescreverá o conteúdo existente. Para preservar e anexar dados existentes, adicione a opção -a .

Por exemplo, salvaremos a saída do comando ping como novas entradas no arquivo test_network.txt :

ping 8.8.8.8 | tee -a test_network.txt
tee-command-imprime-saída-ping-no-terminal-e-um-arquivo
24. comando locate
O comando locate procura um arquivo e imprime seu caminho de localização. Aqui está a sintaxe:

localizar [opções] [palavra-chave]
Se você usar a opção -r para pesquisar arquivos usando expressões regulares, omita o argumento [keyword] . O comando locate diferencia maiúsculas de minúsculas por padrão, mas você pode desativar esse comportamento usando o sinalizador -i .

Note que locate procurará por arquivos de seu banco de dados. Embora esse comportamento acelere o processo de busca, você deve esperar a lista atualizar antes de encontrar itens recém-criados.

Como alternativa, digite o seguinte para recarregar os dados manualmente:

atualizadob
25. comando find
O comando find procura um arquivo dentro de um diretório específico. Aqui está a sintaxe:

encontrar [caminho] [opções] expressão
Se você não especificar o caminho, o comando find pesquisará seu diretório de trabalho atual. Para encontrar arquivos usando seus nomes, adicione a opção -name seguida pela palavra-chave.

Você pode especificar o tipo de item que está procurando usando o sinalizador -type . A opção – type f pesquisará apenas arquivos, enquanto -type d encontrará diretórios. Por exemplo, verificaremos file.txt em path/to/folder :

encontrar caminho/para/pasta -digite f -nome "arquivo"
Diferentemente do locate, o comando find pesquisa pastas em tempo real. Embora ele torne o processo mais lento, você pode procurar por novos itens imediatamente sem esperar que o banco de dados do sistema seja atualizado.

26. comando sudo
superuser do ou sudo permite que usuários não root que fazem parte do grupo sudo executem comandos administrativos. Basta adicioná-lo no início de outro utilitário como este:

sudo [opções] seu_comando
Por exemplo, digite o seguinte para abrir um arquivo usando o nano como administrador:

sudo nano arquivo.txt
O Terminal solicitará que você insira a senha do usuário antes de executar o comando. Por padrão, você deve inseri-la novamente após cinco minutos de inatividade.

Normalmente, você não adiciona nenhuma opção ao sudo, mas pode verificá-las digitando:

sudo --ajuda
Aviso! Como usuários com privilégios sudo podem alterar várias configurações do seu sistema, use este comando com cautela.

27. Comandos su e whoami
O comando su permite que você alterne para outro usuário na sessão Terminal. A sintaxe é a seguinte:

su [opções] [nome de usuário]
Se você não especificar nenhuma opção ou nome de usuário, este comando mudará você para o usuário root . Neste caso, você deve digitar a senha antes de alterar a conta.

Você pode verificar o usuário atualmente logado a partir do shell de linha de comando do Linux. Como alternativa, use o comando whoami :

Uau!
O comando whoami mostra o usuário atualmente conectado
28. comando chmod
Chmod permite que você altere as permissões de arquivos ou diretórios . A sintaxe básica é a seguinte:

chmod [opções] [permissão] [arquivo_ou_diretório]
No Linux, há três permissões de pasta e arquivo – ler ( r ), escrever ( w ) e executar ( x ). Você pode atribuí-las a três partes – o proprietário , um grupo ou outras contas que não pertencem a nenhuma categoria. Considere este exemplo:

chmod -rwx---r-– arquivo1.txt
O ponto após o primeiro hífen ( – ) especifica a permissão para o proprietário de file1.txt . No exemplo anterior, concedemos a eles o privilégio rwx .

O próximo espaço é para grupos. Como não daremos a eles nenhum privilégio, colocamos três hífens para indicar vazio. O último espaço é para outros usuários que têm apenas permissão de leitura ou r .

29. comando chown
O comando chown permite que você altere a propriedade de arquivos, diretórios ou links simbólicos. Aqui está a sintaxe:

chown [opções] novoproprietário:novogrupo arquivo1 arquivo2
Se você quiser atribuir um usuário como o novo proprietário de um item, deixe o nome do grupo em branco. Por exemplo, faremos admin-vps o proprietário de file1.txt :

chown admin-vps arquivo1.txt
Por outro lado, omita o nome de usuário para tornar todos os membros do grupo proprietários. Lembre-se de escrever os dois pontos ( : ) assim:

chown :novogrupo arquivo1.txt
30. Comando useradd, passwd e userdel
Use o comando useradd para criar uma nova conta no seu sistema Linux. A sintaxe é a seguinte:

useradd [opções] novo_nome_de_usuário
Por padrão, o comando useradd não solicita que você forneça uma senha ao novo usuário. Você pode adicioná-la ou alterá-la manualmente mais tarde com o comando passwd :

senha novo_nome_de_usuário
Para remover um usuário, use o comando userdel seguido do nome da conta, como na sintaxe do exemplo:

userdel novo_nome_de_usuário
Como gerenciar outros usuários requer privilégios de superusuário , execute esses comandos como root ou com o prefixo sudo .

Dica profissional
Para definir uma senha e outros detalhes durante o processo de criação da conta, use o comando adduser .

31. comando df
O comando df verifica o uso do disco do seu sistema Linux , exibindo o espaço usado em porcentagem e kilobyte ( KB ). A sintaxe se parece com isso:

df [opções] [sistema de arquivos]
Note que o comando df opera no nível do sistema de arquivos . Se você não especificar um, o utilitário exibirá todos os sistemas de arquivos ativos.

O comando df imprime o uso do sistema de arquivos
32. seu comando
Para verificar o tamanho de um diretório e seu conteúdo, use o comando du . Aqui está a sintaxe:

du [diretório]
O comando verificará seu diretório de trabalho se você não especificar um caminho ou pasta. Por padrão, ele divide o uso de disco de cada subpasta, mas você pode adicionar a opção -s para resumir o uso total em uma saída.

Você também pode usar a opção -M para alterar as informações de KB para MB .

33. comando superior
O comando top exibe todos os processos em execução no seu sistema e seu consumo de hardware. A sintaxe se parece com isso:

topo [opções]
O comando top tem várias opções. Por exemplo, -p permite que você verifique um processo específico especificando seu ID. Enquanto isso, adicione o sinalizador -d para alterar o atraso entre atualizações de tela.

34. comando htop
Assim como top , o comando htop permite que você exiba e gerencie processos no seu servidor Linux . Ele também compartilha a mesma sintaxe:

htop [opções]
htop tem opções similares a top , mas você pode adicionar outras. Por exemplo, -C habilita o modo monocromático, enquanto – -tree mostra processos em uma visão hierárquica.

O comando htop mostra o monitor de desempenho do servidor
35. comando ps
O comando ps resume o status de todos os processos em execução no seu sistema Linux em um momento específico. Diferentemente de top e htop , ele não atualiza as informações automaticamente. Aqui está a sintaxe:

ps [opções]
Você pode imprimir um relatório mais detalhado adicionando outras opções. Por exemplo, use -A para listar todos os processos no seu sistema, -r para verificar apenas os que estão em execução ou -u username para consultar aqueles associados a uma conta específica.

36. comando uname
O comando unix name ou uname exibe informações detalhadas sobre sua máquina Linux, incluindo hardware, nome e kernel do sistema operacional . Sua sintaxe básica se parece com o seguinte:

uname [opções]
Sem nenhuma opção, o comando imprimirá o nome do kernel do seu sistema. Para verificar todas as informações sobre sua máquina, adicione a opção -a .

37. comando hostname
Use o comando hostname para verificar o nome do host do seu VPS e outras informações relacionadas. Aqui está a sintaxe:

nome do host [opções]
Se você deixar a opção vazia, o comando imprimirá seu nome de host. Adicione -i para verificar o endereço IP do seu servidor, -a para imprimir o alias do nome de host e -A para exibir o nome de domínio totalmente qualificado (FQDN) do sistema.

38. comando de tempo
O comando time mede o tempo de execução de comandos ou scripts para obter insights sobre o desempenho do seu sistema. A sintaxe básica se parece com o seguinte:

comando_ou_script_de_tempo
Você pode medir uma série de comandos separando-os usando dois e comerciais ( && ) ou ponto e vírgula ( ; ) assim:

comando de tempo; comando; comando
39. comando systemctl
O comando systemctl é usado para gerenciar serviços no seu sistema Linux. Aqui está a sintaxe básica:

subcomando systemctl [nome_do_serviço][opções]
Os subcomandos representam sua tarefa, como listar, reiniciar, encerrar ou habilitar os serviços. Por exemplo, listaremos os serviços Linux usando isto:

sudo systemctl lista-de-arquivos-de-unidade --tipo-serviço --tudo
Observe que esse comando pode não funcionar com distribuições mais antigas, pois elas usam outro gerenciador de serviços.

O comando systemctl lista todos os serviços
40. comando watch
O comando watch permite que você execute continuamente um utilitário em um intervalo específico para monitorar alterações na saída. Aqui está a sintaxe básica:

assistir [opções] nome_do_comando
Por padrão, watch executará seu comando a cada dois segundos , mas você pode alterar o intervalo usando a opção -n seguida pelo delay. Se quiser destacar as alterações na saída, adicione o sinalizador -d .

41. comando de empregos
Jobs são tarefas ou comandos que estão sendo executados no seu shell atual. Para verificá-los, use o comando jobs com a seguinte sintaxe:

empregos [opções] [ID_do_trabalho]
Executar este comando sem nenhum argumento mostrará todos os trabalhos em execução no primeiro e segundo plano do Terminal. Se você não tiver nenhuma tarefa em andamento, ele retornará uma saída vazia.

Você pode exibir informações mais detalhadas sobre cada trabalho adicionando a opção -l . Enquanto isso, use -n para mostrar apenas tarefas cujo status mudou desde a última notificação.

42. comando kill
Use o comando kill para terminar um processo usando seu ID. Aqui está a sintaxe básica:

matar [opção_de_sinal] ID_do_processo
Para obter o ID do processo, execute o seguinte comando:

ps ux
O comando kill tem 64 sinais de término. Por padrão, ele usa o método SIGTERM que permite que o programa salve seu progresso antes de fechar.

43. comando shutdown
O comando shutdown permite que você desligue ou reinicie seu sistema Linux em um horário específico. Aqui está a sintaxe:

desligamento [opção] [hora] [mensagem]
Se você executar o comando sem argumentos, seu sistema será desligado imediatamente. Você pode especificar o agendamento usando um formato de 24 horas ou um relativo. Por exemplo, digite +5 para desligar o sistema após cinco minutos . Para reiniciar a máquina, adicione a opção -r .

O argumento da mensagem especifica a notificação que outros usuários no seu sistema receberão antes do servidor ser desligado.

44. comando ping
O comando ping envia pacotes para um servidor de destino e busca as respostas. Ele é útil para diagnósticos de rede. A sintaxe básica se parece com a seguinte:

ping [opção] [nome_do_host_ou_endereço_IP]
Por padrão, o ping envia pacotes infinitos até que o usuário o interrompa manualmente pressionando Ctrl + C .

No entanto, você pode especificar um número personalizado usando a opção -c . Você também pode alterar o intervalo entre transferências adicionando -i .

Por exemplo, vamos enviar 15 pacotes a cada dois segundos para o servidor do Google:

ping -c 15 -i 2 google.com
O comando ping envia pacotes para o Google com configurações personalizadas
45. comando wget
O comando wget permite que você baixe arquivos da internet via protocolos HTTP, HTTPS ou FTP. Aqui está a sintaxe:

wget [opções] [URL]
Por padrão, o comando wget baixará um item para seu diretório de trabalho atual. Por exemplo, execute este comando para recuperar o instalador mais recente do WordPress:

wget https://wordpress.org/latest.zip
46. ​​Comando cURL
Use o comando cURL para transferir dados de ou para um servidor especificando sua URL. A sintaxe básica é a seguinte:

curl [opções] URL
Executar cURL sem uma opção imprimirá o conteúdo HTML do site no seu Terminal. Se você adicionar a opção -O ou -o , o comando baixará os arquivos do link especificado.

O comando cURL também é útil para testar endpoints de API ou servidor. Você pode fazer isso adicionando a opção – X seguida por um método HTTP , dependendo se você deseja buscar ou carregar dados.

Por exemplo, o comando a seguir recuperará dados de um ponto de extremidade de API específico:

curl -X GET https://api.example.com/endpoint
47. comando scp
O comando scp permite que você copie arquivos e diretórios com segurança entre sistemas em uma rede. A sintaxe é a seguinte:

scp [opção] [nome de usuário de origem@IP]:/[diretório e nome do arquivo] [nome de usuário de destino@IP]:/[diretório de destino]
Se você estiver copiando itens de ou para sua máquina local, omita o IP e o caminho. Ao transferir um arquivo ou pasta de uma máquina local, especifique seu nome após as opções.

Por exemplo, executaremos o seguinte para copiar file1.txt para o diretório path/to/folder do nosso VPS como root:

scp file1.txt root@185.185.185.185:caminho/para/pasta
Você pode alterar a porta SCP padrão especificando seu número após a opção -P . Enquanto isso, use o sinalizador -l para limitar a largura de banda de transferência e adicione – C para habilitar a compactação.

48. comando rsync
O comando rsync sincroniza arquivos ou pastas entre dois destinos para garantir que eles tenham o mesmo conteúdo. A sintaxe é a seguinte:

rsync [opções] origem destino
A origem e o destino podem ser uma pasta dentro do mesmo sistema, uma máquina local ou um servidor remoto. Se você estiver sincronizando conteúdo com um VPS, especifique o nome de usuário e o endereço IP assim:

rsync /caminho/para/pasta/local/ vps-user@185.185.185.185:/caminho/para/pasta/remota/
Você pode adicionar a opção -a para sincronizar os atributos do arquivo ou pasta também, incluindo seus links simbólicos. Enquanto isso, use o sinalizador -z para habilitar a compactação durante a transferência.

49. comando ip
O utilitário ip permite que você liste e gerencie os parâmetros de rede do seu sistema, similar ao comando ifconfig em distros Linux mais antigas . Aqui está a sintaxe:

comando objeto ip [opções]
Executar este comando sem nenhum argumento imprimirá o manual, incluindo uma explicação sobre opções e objetos aceitáveis.

Para gerenciar um parâmetro de rede, especifique a ação no argumento command . Por exemplo, execute isto para mostrar o endereço IP do seu sistema:

mostrar endereço ip
O comando ip mostra as informações do endereço IP do sistema
50. comando netstat
O comando netstat exibe informações sobre a configuração de rede do seu sistema. A sintaxe é simples:

netstat [opções]
Adicione uma opção para consultar informações específicas da rede. Aqui estão vários sinalizadores para usar:

-a – exibe soquetes de escuta e fechados.
-t – mostra conexões TCP.
-u – lista conexões UDP.
-r – exibe tabelas de roteamento.
-i – mostra informações sobre interfaces de rede.
-c – emite continuamente informações de rede para monitoramento em tempo real.
51. comando traceroute
O comando traceroute rastreia o caminho de um pacote ao viajar entre hosts, fornecendo informações como o tempo de transferência e roteadores envolvidos. Aqui está a sintaxe:

traceroute [opções] destino
Você pode usar um nome de host, nome de domínio ou endereço IP como destino. Se você não especificar uma opção, o traceroute executará o teste usando as configurações padrão.

Altere os saltos máximos de pacotes usando a opção -m . Para evitar que o traceroute resolva endereços IP, adicione -n ​​.

Você também pode habilitar um tempo limite em segundos usando o sinalizador -w seguido pela duração.

52. Comando nslookup
O comando nslookup solicita que um servidor de sistema de nomes de domínio (DNS) verifique um domínio vinculado a um endereço IP ou vice-versa. Aqui está a sintaxe:

nslookup [opções] domínio-ou-ip [servidor-dns]
Se você não especificar um servidor DNS, o nslookup usará o resolvedor padrão do seu provedor de serviços de internet. Você pode adicionar outras opções para alterar como esse comando consulta um endereço IP ou um domínio.

Por exemplo, use a opção -type= para especificar as informações que deseja verificar, como os registros DNS.

Você também pode configurar a repetição automática com o sinalizador -retry= e adicionar -port= para usar uma porta específica.

O comando nslookup resolve um nome de domínio para um endereço IP
Como algumas distros Linux não têm esse utilitário pré-instalado, você pode encontrar o erro “command not found” . Você pode configurá-lo baixando bind-utils ou dnsutils por meio do seu gerenciador de pacotes.

53. comando dig
O comando domain information groper ou dig exibe informações sobre um domínio. É semelhante ao nslookup , mas mais abrangente. A sintaxe é a seguinte:

dig [opções] [servidor] [tipo] nome-ou-ip
Executar dig sem um argumento verificará os registros A do domínio especificado usando o resolvedor padrão do sistema operacional. Você pode consultar um registro específico especificando-o no argumento [type] como no exemplo a seguir:

dig domínio MX.com
Para executar uma pesquisa reversa de DNS, adicione a opção – x e use um endereço IP como destino.

54. comando de história
Execute o comando history para verificar utilitários executados anteriormente. Aqui está sua sintaxe:

história [opções]
Adicione a opção -r se quiser limpar o histórico do Terminal. Para executar novamente um utilitário específico da lista, insira um ponto de exclamação seguido de seu ID.

Por exemplo, use o seguinte para executar o 145º comando:

!145
comando history imprime histórico do terminal
55. comando do homem
O comando man ou manual exibe um guia abrangente de outro utilitário. A sintaxe se parece com a seguinte:

homem [opções] [número_da_seção] nome_do_comando
Se você especificar apenas o nome do comando, man exibirá o manual inteiro. Alternativamente, você pode selecionar uma das nove seções usando seus IDs para imprimir informações mais específicas.

Por exemplo, execute o seguinte para verificar a seção de chamada de biblioteca do manual do comando ls :

homem 3 ls
56. comando echo
Use echo para imprimir texto no seu comando como uma saída do Terminal. Aqui está a sintaxe:

eco [opções] [texto]
Você também pode adicionar o símbolo de redirecionamento ( > ) para imprimir o texto em um arquivo em vez do Terminal. Se você usar dois símbolos ( >> ), ele anexará o conteúdo existente. A sintaxe do comando se parece com isso:

echo [opções] [texto] > [nome_do_arquivo]
Se o seu texto contiver uma variável de ambiente ou shell como $var , echo exibirá o valor real. Este comando é comumente usado para testes e scripts bash .

57. Em comando
O comando ln vincula arquivos ou diretórios com um atalho. A sintaxe é a seguinte:

ln [opções] origem destino
Este comando criará o atalho automaticamente, o que significa que você não precisa fazer um manualmente. Por exemplo, o seguinte permitirá que você abra file.txt usando shortcut.txt :

Em target.txt shortcut.txt
Por padrão, ln cria um hard link, o que significa que alterações na fonte serão refletidas no item vinculado e vice-versa. Para configurar um soft link ou simbólico, adicione a opção -s .

58. Comando alias e unalias
O comando alias permite que você defina outro nome para uma string que pertence a um arquivo, texto, programa ou nome de comando. Aqui está a sintaxe:

nome do alias='string'
Por exemplo, o seguinte atribuirá k como o alias para o comando kill , permitindo que você use a letra em vez do nome completo.

alias k='matar'
Para verificar o alias de um comando, execute alias seguido por um nome alternativo. Por exemplo, verificaremos o snippet anterior:

alias k
alias commands mostra uma letra associada a um comando
Você pode remover um alias executando esta sintaxe:

unalias [nome]
59. comando cal
O comando cal exibe um calendário na sua interface de linha de comando do Linux. Aqui está a sintaxe:

cal [opções] [mês] [ano]
Se você não adicionar nenhum argumento, o comando mostrará a data atual. Alternativamente, você pode digitar um mês e ano específicos em um formato numérico.

Você também pode adicionar a opção -3 para mostrar o mês atual, o anterior e o próximo.

60. Comando apt e dnf
O comando apt permite que você gerencie bibliotecas de ferramentas avançadas de pacotes (APT) em sistemas operacionais baseados em Debian, como Ubuntu e Kali Linux . A sintaxe se parece com isso:

subcomando apt [opções]
Os subcomandos definem a ação, como atualizar a biblioteca, atualizar o software, instalar um aplicativo ou remover um pacote. Por exemplo, instalaremos o editor de texto Vim :

apt instalar vim
No Linux, os comandos de gerenciamento de pacotes diferem entre as distribuições. Por exemplo, distros baseadas no Red Hat Enterprise Linux como CentOS e AlmaLinux usam dnf . Ele tem a mesma sintaxe e opções que apt .

Executar apt e dnf requer privilégios de superusuário , que você só pode obter com sudo ou via root .
