# COMMITS #

* `git commit -m "mensagem do commit"`
(commitar o projeto com mensagem)

* `git commit -a -m "mensagem do commit"`
(pula a etapa de add ao stage e commita direto)

* `git checkout -- nome do aquivo` 
(voltar o arq. original do ultimo commit)

* `git rm nome do arq.` 
(deleta o arquivo sem volta, e resolve conflito no stage em caso de remoção dos arq. do último commit)

* `git log`  
(histórico de commit com hora + usuário)

* `git log -p` 
(histórico detalhado dos commits)

* `git log -p -1` 
(último commit detalhado)

* `git log --pretty=oneline`  
(mostar a chave de cada commit e a mensagem)

* `gitk`  
(abre interface gráfica)

* `git commit --amend -m "novo nome do commit"` 
(substitui último commit feito com o commit atual)
