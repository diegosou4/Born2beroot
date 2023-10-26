# Born2beroot

## Debian ou Rocky o primeiro passo.

## Debian
Debian quando lanca sua atualizacao faz testes de estresses em seu software antes de lancar ao usuario, eles tem um grande
cuidado na hora de lancar uma atualizacao, assim evitando uma grande quantidade de bugs e o mais interessante
e que nao precisamos reiniciar a maquina depois de uma atualizacao ele usa o gereciador de pacotes apt, exceto quando precisamos
atualizar o kernel do debian, porem atualizacoes do kernel sao raras e voce pode agendar.

Debian tem uma grande compatibilidade com dispositivos e hardware de servidores.

O Debian tem um gerenciamento de pacotes melhor e mais flexivel comparando ao CentOs.

## Rocky Linux CentOS
E uma das distribuicoes linux mais antigas tendo mais de 18 anos ativa.

O Rocky linux e mais densevolvido para empresas, ela e mais recente no mercado, seu lancamento foi em 2021
ele usa uma variante do centos, ela e baseada em uma distribuicao linux que esta em pausa de atualizacao ate 2024

Atualizar para ultima versao e mais complicado que parece ate os funcionarios tem dificuldades em fazer, preferem reistalar do zero.
Alguns aplicativos atualizados ficam bugados, porque o centos demora muito para atualizar sendo assim o usuario tem que usar aplicativos em versoes mais antigas.

Na hora de instalar o debian so contem os arquivos ensenciais enquanto o centos pensa na interface do usuario.
APT -  Advanced Package Tool


### 

LVM - Logical Volume Management



links interessantes [https://www.redswitches.com/blog/centos-vs-debian/] [https://www.redhat.com/pt-br/topics/linux/what-is-centos] [https://www.fosslinux.com/46040/reasons-use-debian-linux-distro.htm] [https://www.pontikis.net/blog/five-reasons-to-use-debian-as-a-server#google_vignette]




### O que sudo
Existe um comando chamando `su` que quando voce digita no prompt de comando e apos ele coloca o nome de outro usuario registrado

/etc/sudores 



### Comandos


sudo adduser "nome do user" -- vai criar um novo usuario

su "nome do user" -- voce vai trocar de usuario na maquina 



quando faco 
sudo usermod -a -G sudo diegmore

a flag -a (--append) indica que o usuario deve ser adicionado ao grupo sem remover ele de qualquer outro grupo que ele esta includo 
a flag -g (--groups)e usado para espeficar que aquele usuario vai ser adicionado em um ou mais grupos

estou colocando o diegmore no grupo de superusuarios

Basicamente quando eu coloco o usuario no grupo sudo, a partir de agora quando ele executar o comando sudo , ele vai conseguir
fazer o que usuario root faria naquele momento, entao basicamente eu posso ter um usuario dentro do meu linux que nao possui essa permissao,
isso e interessante quando voce nao quer que o usuario instale arquivos que necessitam dessa permissao.

Mesmo colocando meu usuario no grupo de sudores existem arquivos que pelo fato terem informacoes sensiveis ele ainda 
e necessario que eu chame o sudo antes de tentar ler,editar o arquivo, ou seja o usuario root que realmente pode fazer isso.




getent serve como um atalho para voce ver o que tem dentro do banco de dados (repositorios) do seu linux e uma forma mais facil do que voce precisar cd /etc/group
para verificar quais bancos de dados e tipos que existem voce pode da um cat /etc/nsswitch.conf , voce vai encontrar um arquivo mostrando os bancos que tem o tipo deles.
dentro desse arquivo vao ter passw, groups , shadow que sao um banco de dados (file-based-database), ou seja um banco de dados que armazena dados de um arquivo de forma simples, 
vai encontar hots como file dns que basicamente a mesma coisa porem contem informacoes relacionadas a dns.


``
You need to edit /etc/sudoers. For those who don't use vi, 
you should edit this file (on some flavors of Linux) with a terminal command like this:
sudo EDITOR=gedit visudo
``


## Particoes

A Particao swap normalmente ela e configurada para 1 GB, e interessante porque caso o computador esteja precisando de memoria ram
ele faz um swap de 1gb de hd para ram, assim evitando sobrecarga, ela da esse 1 giga porem a particao swap ela vai ser muito mais lenta do que a memoria ram.
Ou seja ajuda, naquele momento de estresse, mas dependendo do estresse nao vai ajudar tanto.

A Particao Raiz / 
No caso da nossa particao root, sim o usuario root esta na particao raiz por que ele e um superusuario do sistema assim vai ter o diretorio do usuario root e do sistema e vai 
conter todos os diretorios do sistema que ele pode acessar e controlar.


A Particao temp /temp
Aonde ficam todos os arquivos temporarios gerados pro progamas e o sistema que nao vao ser usados depois de ser executado, apois reiniciar ele automaticamente vai apagar esses arquivos

A Particao srv /srv
Aonde vao ficar os dados e arquivos do servidor web que voce criou

A Particao var
Aonde vao ficar arquivos que estao sempre em constante alteracao durante a operacao do sistema

A particao var/log
e uma subpasta dentro da var, que armazena os logs , ou seja as informacoes dos aplicativos e tudo que ta rodando, para caso tenha algum erro ele guarda para voce
