# REPOSITORIO REMOTO EM MAQUINA VITUAL #

* > Com servidor local em maquina virtual rodando windowns

* Dentro da pasta do repositório server criar pasta "projetos1"

* Agora vamos dar acesso a essa pasta via rede

* Ver nome da máquina em painel de controle > sistema e segurança > sistema

* Abrir configurações de sistema

* Depois va em: proteção do sistema > nome do computador > nome completo do computador : vmserver (nome da máquina como servidor remoto)

* Ou pode ser acesso por ip também

* Agora botão direito na pasta projetos criada > compartilhar com > pessoas específicas > todos > adicionar > permissão: leitura e gravação > compartilhar

* Se for agora na sua máquina e colocar > na barra de url em meu computador > digitar \\vmserver > enter > agora vai aparecer a pasta projetos dentro do repositório em rede, isso fez um acesso via rede a esta pasta

* > *EX: dentro da pasta projetos criar "cliente1" essa sera a pasta a ser trabalhada e compartilhada em equipe

* Instalar o git na máquina do servidor

* Entrar na pasta "cliente1" e iniciar o git init --bare 
(vai criar um monte de pastas pois o repositorio foi iniciado em modo "bare")

* `git init` 
(repositorio pardão não aconselhado quando se trabalha com equipes)

* `git init --bare`
(mais aconselhado quando se trabalha em equipe)

* Voltando para o pc de desenvolvimento

* Primeiro acesso no terminal exige essa config.: 
`git clone file:////vmserver/projetos/cliente1`

* > Isso vai clonar o que esta no servidor remoto e trazer para sua máquina local na pasta atual. 
Caso voce queira mudar o nome da pasta clonada adicionar nome no final ficando assim:
`git clone file:////vmserver/projetos/cliente1 prjrede1`

* > Isso vai clonar dentro da pasta prjrede1 todos os arq. do servidor remoto

* Na sua pasta local colocar arq. base dos sistema add e commitar

* > Porém os arq. ainda não estao no servidor remoto, se clonar novamente com nome prjrede2, irá clonar o projeto vázio

* > Para enviar o commit do prjrede1 para o servidor remoto sera necessário o push

* > Para isso precisa saber o nome do remote, com:
`git remote` 
* > Por padrão ele coloca o nome do remote como `origin`

* > Entao para enviar o commit da máquina prjrede1 para o servidor remoto, fazer:
`git push origin master`
(git envia os arq. para o servidor origin que estão na branch master)

## < Aguardar... > ##

* > Testar agora os arquivos enviado ao servidor remoto, note que se voce entra na pasta do servidor elas vao aparecer diferentes do repositorio da máquina, porque sua estrutura de pastas é diferente estão em modo --bare, os arquivos enviados estarao dentro de "objects"
