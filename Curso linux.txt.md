###### informações iniciais

linux criado em 1991 por lin
us torvalds
linux é o kernel ( núcleo do sistema)
software livre
multitarefa/multiusuário

shell ou terminal:

usado para automação de tarefas via linha de comando

###### terminal:

usuário roots                                      é o que possui mais privilégios no linux.

adduser + nome de  usuário           para criar um novo usuário

sudo                                                       para elevação de permissão



###### comandos:

ctrl + alt + t           abre o terminal

pwd                     mostra o caminho onde estamos na pasta

comando ls       visualiza arquivos dentro da pasta

cd                        muda o diretório

"~"                       mostra que vc esta na pasta principal

mkdir                  cria nova pasta

cd ..                     volta uma pasta

cd dir                  muda para o diretório digitado

rm -r                   remove diretório

/                          diretório raiz do sistema, similar ao c:

ls -l                      vê os diretórios com detalhes

ls + nome                 lista um diretório que não seja o corrente 

man + comando               abre a explicação do que o comando faz

q                                           sai do manual

history                exibe histórico de todos os comando digitados no terminal

!!                            executa o ultimo comando digitado no terminal

###### Atalhos do terminal



ctrl + C        Cancela o comando atual em funcionamento

ctrl + z         Pausa o comando atual, em primeiro plano ou segundo plano

ctrl + d        Faz logout da sessão atual (sai do terminal)

ctrl + w        Apaga uma palavra na linha atual

ctrl + u         Apaga a linha inteira

ctrl + r         Busca um comando recente

!!                   Repete o ultimo comando

exit              Sai do terminal

mv +  nome + local               Move o diretório ou arquivo

mv + nome da pasta + novo nome          Para renomear a pasta

touch+ nome arquivo         Cria arquivos vazios

cp nome arquivo + local novo               Faz uma copia do arquivo

cd  + inicio do arquivo + Tab                  Vai ate a pasta

rmdir+ nome                          Remove diretório/ tbm serve para apagar arquivos

clear                                          Limpa a tela

comando +--help                    exibe o arquivo de ajuda de um comando

man + comando                     exibe o manual do comando

###### aula "Fuçando que se aprende"

historiy -c                                         limpa o histórico de comandos

alias + apelido='comando'          da um nome "apelido" para um comando

nl + nome arquivo          exibe o arquivo com o numero de linhas de um arquivo                    

wc -l +nome                       conta linhas com linhas em branco

wc -w+nome                      conta numero de palavras

wc -c+nome                        conta os bytes

wc -m                                   conta os caracteres

ls -a                                      exibe arquivos ocultos na pasta

ls -F                                      põe uma / em frente dos arquivos

cat +nome                         visualiza o que tem no arquivo

cmp  nome  nome           compara dois arquivos

diff  nome nome              mostra diferença entre arquivos

sort -n                                 organiza a saída do arquivo em ordem numérica

cal                                        mostra o calendário do mês corrente

date                                     mostra data de hoje

###### Editando arquivos de texto

nano +nome                     abre o arquivo no nano

###### MENU NANO

  ^G                                     ajuda

 ^O                                      grava 

 ^W                                     onde esta?

^K                                        recort txt

^R                                        lê o arquivo

^X                                        sair

obs:  mais comandos no rodapé do nano

cat +nome arquivo         visualiza o conteúdo de um arquivo   

tac +nome arquivo         visualiza de forma invertida   

head +nome arquivo     mostra as 10 primeiras linhas

tail + nome arquivo        mostra as 10 ultimas linhas do arquivo

###### comandos de redirecionamento

tail +nome arquivo >   nome arquivo 2       cria um novo arquivo com nome do segundo arquivo contendo as 10 ultimas linhas do primeiro arquivo



head +nome arquivo >   nome arquivo 2       cria um novo arquivo com nome do segundo arquivo contendo as 10 primeiras linhas do primeiro arquivo

informação > arquivo        cria e substitui informações no arquivo

informação >> arquivo      adiciona a informação no arquivo selecionado

|    (pipe "barra em pé)                         para usar 2 comandos juntos  

| more                                                     faz paginação do arquivo

| less                                                        também faz paginação do arquivo

&                                                             separa por linha os arquivos abertos

&&                                                          funciona como and

file                                                           mostra o tipo de arquivo  

whatis                                                     diz o que o comando faz

find + pasta  -name arquivo             busca o caminho de um arquivo

grep + item + nome arquivo             busca o item no arquivo selecionado

mv + nome antigo + nome novo      troca o nome do arquivo

rm -r *                                                     remove todos os arquivos de uma pasta

#### Diretórios

/bin/                                                      binário (exe) principal dos usuários

/boot/                                                   arquivos do sistema de boot

/dev/                                                     arquivos dos dispositivos

/etc/                                                      arquivos conf. do sistema

/home/                                                 diretório usuários comuns

/lib/                                                        bibliotecas e módulos do kernel

/media/           /mnt/                          montagem de dispositivos

/opt/                                                     instalação de programas não oficiais

/sbin/                                                    executáveis

/srv/                                                       dados de serviços fornecidos pelo sistema

/tmp/                                                      arquivos temporários

/usr/                                                       segunda hierarquia do sistema

/var/                                                       variáveis gerados por programas

/root/                                                     diretório usuário root (administrador)

/proc/                                                    diretório virtual controlado pelo kernel

lspci                                                       mostra hardwares conectados via pci

arch                                                       mostra a arquitetura do sistema

uname -r                                              mostra versão do kernel

free                                                        mostra saída de memoria 

du -h + diretório                        ver quantidade de memoria usada pelo diretório

cat /etc/passwd                        mostra todos os usuários do sistema

reboot                                                  reinicia o sistema

shutdown  -h + now             desliga o sistema

lscpu                                             mostra todas as informações da cpu

lshw                                           mostra lista de todos os hardwares que encontrar

lshw -short                              mostra caminho dos hardwares



#### Fundamentos de redes

Wan                                      rede de cobertura mundial (internet)

Man                                      rede metropolitana  (interligam as Lans)

Lan                                       rede local   (casa, ou empresa etc...)

Protocolo Linguagem utilizada pelos dispositivos para se comunicar entre si.

IP    Protocolo de internet - Endereço IP- numero que identifica seu computador em uma rede



ICMP (Internet Control Menssage Protocol) Promove mensagens de controle na comunicação entre nós



DNS (Domain Name server) Identifica endereços IPs mantem uma tabela com endereços dos caminhos de algumas redes

interface de rede em linux fica no diretório /dev/.

eth0 eternet

loopback tipo essencial de interface que permite testar programas e softwares sem interferir na sua rede ou servidor. 127.0.0.1

ifconfig        saber IP da maquina mas é preciso instalar o pacote antes

sudo apt install net-tools           comando para instalar 

mascara de rede       numero de 32 byts que separa minha rede da rede local

broadcast                   endereço publico de rede local se mandar msg todos os computadores da rede recebem

ipv6   IP em hexadecimal 

ether   "endereço mac" endereço da placa de rede, único para cada computador

loopback endereço local

hostname       mostra o nome do computador na rede

hostname -I      mostra o endereço do computador na rede

hostname -i    mostra o endereço de loopback

who                  como estamos logados na rede

whoami           nome do usuário logado na rede

ping                 verifica se o host esta ativo ou inativo

ping -w + numero    envia uma quantidade de pacotes limitada

sair ctrl+z

dig   comando que tras informações sobre DNS

traceroute      traça a rota ate o caminho desejado ( precisa ser instalado)

traceroute +endereço(www...)    mostra caminhos e os nós ate chegar no endereço

dig +endereço (+short)  trás só o DNS do endereço

whois  (precisa de instalação)   mostra informações sobre determinado site como domínio, id, pais, servidor, contato etc....

finger (precisa instalar)     mostra toda informação do usuário logado no host

 #### Controle de usuários, Grupos e Permissões

adduser + nome do usuário                      criar um novo usuário

su +nome do usuário                                    trocar o usuário (precisa da senha)

passwd + nome do usuário         trocar senha do usuário (precisa senha antiga)

criando senha segura = não usar números sequenciais nem números de documentos, nuca por nome de parente, adimin etc...

"Zenit Polar" usar troca de letras. Boas senhas tem em media 8 caracteres ou mais com letras maiúsculas, minúsculas e números.

lastlog   exibir informações de login

last         exibe listagem de entradas e saídas de usuários no sistema 

logname                exibe nome do usuário atual logado no sistema

id                             exibe todos os identificadores do usuário

cat/etc/passwd    exibe todos os usuários

###### Remover usuário e pasta do mesmo 

userdel -r nome do usuário         remove o usuário e a pasta pessoas dele

##### GRUPOS

cat/etc/group                                 exibe todos os grupos no sistema

groups                                              exibe grupos do usuário atual

addgroup                                         adiciona um grupo novo (só o root pode)

sudo adduser +nome +grupo                            adiciona um usuário ao grupo

sudo gpasswd -a + nome + grupo                     adiciona um usuário ao grupo

sudo gpasswd -d + usuário +grupo                  remove usuário do grupo

sudo groupdel + nome do grupo                     remove um grupo

#### Permissões

Permissões em arquivos e diretorios servem para restringir acessos como:

leitura, escrita e execução onde:

r -read (leitura)

w -write(escrita)

x - execution (execução)

chmod + n° + arquivo                      muda a permissão de um usuário   



 user (owner)         group            other

​     r    w   x              r   w   x            r  w  x        

​     4    2   1              4    2  1            4   2   1   

###### comandos Variados

las reboot               informações sobre reinicialização do sistema

route -n                  mostra todas as tabelas de roteamento IP do Kernel

time +comando                       tempo de um processo

up time                                      mostra o tempo que o sistema esta rodando

cowsay     (precisa instalar)     cria uma vaquinha que fala

cowsay -d                                     vaquinha doente

cowsay -g                                     vaquinha com $ nos olhos

cowsay - f                                    outros bichinhos

xcowsay (precisa instalar)      vaquinha 3D

cmatrix  (precisa instalar)       chuva de caracteres como no matrix

init 0                                             desliga a maquina

telinit 0                                         desliga a maquina agora

halt                                                pede autenticação pra desligar a maquina

seq  n°+ n°                                              imprime uma sequencia de números

#### Compactação Descompactação e argumentos

extensões : 

.pptx       power point

.pdf         arquivo "não editável"

.rar          compactador de arquivo

.zip          compatador de arquivo

gzip + nome do arquivo                        para compactar o arquivo

gunzip +nome do arquivo + .gz           para descompactar o arquivo

gzip -9 + nome do arquivo                   para compactação máxima do arquivo

zip + arquivo.zip + arquivo                   para compactar com zip

zip + nome.zip + arquivo+arquivo      para compactar mais de um arquivo

unzip + nome.zip                                    descompactar o arquivo sem remover

rm + arquivo.zip                                     para remover 

bzip2 + arquivo                                       para compactar com bzip2

bzip2 -d + arquivo.bz2                           para descompactar bzip2

rar (precisa instalar)

rar +a+ arquivo.rar + arquivo              para compactar com rar

rar+ x + arquivo.rar                                para descompactar

rm + arquivo.rar                                      para remover o arquivo depois 

###### Arquivadores

tar  -cf + arquivo.tar + arquivo             para arquivar com tar

tar -xvf + arquivo.tar.gz                    para descompactar um arquivo tar zipado 

tar -xvf + arquivo.tar.gz -c +endereço           para descompactar para outro endereço

#### Gerenciamentos de pacotes

extensões de pacotes mais comuns      .deb,  .rpm

exemplos de gerenciadores: (sistemas que possuem automáticas de dependências entre pacotes) apt,  dpkg, yum e rpm

sudo apt install + pacote                     instalar com gerenciador apt

sudo apt upgrade + pacote                para atualizar um pacote no sistema

sudo apt remove + pacote                 para remover um pacote

sudo apt update && apt upgrade    (precisa trocar para root com sudo su antes)

ai ele fará atualização do sistema.

sudo dpkg -i                                             para instalar pacotes .deb

sudo dpkg -I + pacote.deb                   ver a discrição do pacote

sudo dpkg -r + nome do pacote ( nome é dado na descrição do pacote)

para desinstalar um pacote com dpkg

Gerenciadores de pacote no Fedora

rpm -ivh + pacote.rpm                   para instalar pacotes com extensão rpm

sudo rpm - ivh -- nodeps + pacote     para resolver problema de dependências

sudo rpm -U +pacote                                         para atualizar pacote rpm

sudo rpm -e + pacote.rpm                                para remover o pacote

sudo yum install +pacote                                   para instalar pacote yum

sudo yum update + nome do pacote              para atualizar o pacote  

sudo yum remove + nome do pacote             para remover o pacote













​        

















​                                                              

 



​                        

