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

a flag -a indica que o usuario deve ser adicionado ao grupo sem remover ele de qualquer outro grupo que ele esta includo 
a flag -g e usado para espeficar que aquele usuario vai ser adicionado em um ou mais grupos

estou colocando o diegmore no grupo de superusuarios




