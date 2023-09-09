/* Enquanto eu não tenho arquivo nenhum, meu repositório
   vai acusar que eu não tenho nada mesmo. 

On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md
        pedro

nothing added to commit but untracked files present (use "git add" to track) */




Desse jeito aqui !!

Então ele vai estar " Untracked " no caso, ele ainda não consegue ver
o arquivo sendo localizado na pasta. Mesmo, ele já criado.



On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Readme.md
        
        
/* Agora ele já está add no git, e visto por ele, podendo ser
a qualquer momento modificado */ 



/* Agora, se eu alterar aqui no meu arquivo algo, para acrescentar ou tirar
vai acusar lá no *Git Status* e para eu carregar essa atualização comigo
, eu preciso digitar novamente o comando de add : 

git add nome_do_arquivo */


 Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Readme.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md
        
        
 git add Readme.md 
 
 git status
 
 On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Readme.md
        
        
 /* Ele volta ao normal, com a última atualização */
 
 
 Agora vamos commitar !
 
 O que é commitar - é salvar o arquivo na fase que ele já está " pronto ".
 
 
 ok, vamo lá :
 
 ( Se você alterou o documento, não esqueça de salvar as alterações )
 ( verifique no : git status )
 ( git add nome_do_arquivo )
 ( verifique de novo. )
 
 Se estiver tudo ok, committe .
 
 git commit -m "Salvar arq" 
 
 (-m) é para deixar uma mensagem salva nele, para quem ver esse doc
 saber se localizar quando entrar nele.
 
 O resultado:
 
 [master (root-commit) 9d3f9e1] salvar arq
 1 file changed, 93 insertions(+)
 create mode 100644 Readme.md





git config --global user.name "nome" ( add um nome ao seu novo git )

git config --global user.email "email" ( add um email ao seu novo git )

git config --global core.editor editor_que_você_usa 

git init ( para iniciar para o git a sua pasta ou trabalho )

git add comandos_git.md ( add os comandos, para o git começar a enchegar )

git status ( para ver como está os status das pastas, se tem algumas que precisam salvar e tals )

git commit -m "qualquer_mensagem" ( usa para comunicar todos que vão usar o matérial, se localizarem onde foi feito
uma alteração. )

git commit -am " Edite_comandos_git.md " ( Se o arquivo já existir, e eu querer commitar de novo. Eu tenho que colocar
-am, para eu salvar como um novo commit ) 
 


git log ( mostra algumas informações importantes )

git log --author "nome_de_alguem" ( mostra todas os commit que tem no nome da pessoa, e seu dados )

git shortlog ( mostra para gente, quais são os autores em ordem alfabética , e quantos commit fizeram e quais foram )

git shortlog -sn ( mostra apenas, quais são os autores e o número de commit que eles fizeram )

git log --graph ( vamo ver mais pra frente )

TODO GIT TEM UMA HASH. ( um número grande abessa, do lado do commit. )

MAS ATRAVÉS DESSA HASH, PODEMOS VER AS ALTERAÇÕES FEITAS NO COMMIT PARA NÃO PERDERMOS NADA, QUANDO ATUALIZARMOS NOSSO REPOSITÓRIO 

git show núm_da_hash ( vai aparecer tudo que eu disse em cima ) 


git diff ( lista todas as suas últimas alterações no código, antes de você " add ele novamente ( git add ) e comitar ( git commit -m "mensagem" ) )

/* E ele ainda, te mostra a sua última alteração, e o que você escreveu de novo. */

git diff --name-only ( Demonstra para você, apenas os nomes do arquivo que foi modificado )




DESFAZENDO AS COISAS 

Se eu quiser desfazer, uma alteração que eu fiz no meu git, antes do ( git add ), eu uso :

git checkout nome_do_arquivo ( Ele faz com que, o arquivo volte para como era antes da última edição ) 


Agora, eu salvei o arquivo e quando eu fui ver, não gostei muito, quero mudar, tem como ? Sim, têm como !

git reset HEAD ( O head, é como se eu estivesse falando " eu não quero ter meu git no meu stage " , mas ele volta para última vez )

git reset --soft ( Ele vai matar meu commit, pegar as modificações ( voltar para o stage ) e deixar prontinho para commitar de novo )

git reset --mixed ( Ele vai matar meu commit, mas ele vai voltar para antes do stage, modified, para add novamente e depois committar )

git reset --hard ( Ele vai matar tudo, e voltar para onde eu apontei a hash )


commit dd8415f23d9b36afde5a0445febf7eaf7bb4680b (HEAD -> master)
Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 17:48:52 2023 -0300

     qual foi

commit f1282559a09c62b8f5c50ccbaa8bcf5b6b1871ca
Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 17:27:22 2023 -0300

     Edit comandos



Se eu quero tirar o git " qual foi ". Eu preciso começar os comandos apartir do Edit comandos .
 
Porque, quando eu der o reset, o git " qual foi " já não vai existir, então o meu git de partida vai ser o Edit comandos.
 
 

git reset --soft f1282559a09c62b8f5c50ccbaa8bcf5b6b1871ca
 

(vai sumir o commit " qual foi " e ficar apenas o " Edit comandos " , pronto para commitar na staged)


pp918545@penguin:~/git-course$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   comandos_git.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   comandos_git.md
        
        


git reset --mixed 

commit fa508d2c4ad3a97e09ec16f91d2d5c83f7342a9d (HEAD -> master)
Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 18:12:21 2023 -0300

     ok agora


commit f1282559a09c62b8f5c50ccbaa8bcf5b6b1871ca
Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 17:27:22 2023 -0300

     Edit comandos
     
     
          
git reset --mixed f1282559a09c62b8f5c50ccbaa8bcf5b6b1871ca

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   comandos_git.md
        
        
        
Ele está pronto para ser modificado, não estando no staged .

Então, se dermos um " git diff " vai aparecer as últimas modificações feitas no arquivo.


diff --git a/comandos_git.md b/comandos_git.md
index 4b6032f..dd295f4 100644
--- a/comandos_git.md
+++ b/comandos_git.md
@@ -41,3 +41,93 @@ git diff ( lista todas as suas últimas alterações no código, antes de você
 
 git diff --name-only ( Demonstra para você, apenas os nomes do arquivo que foi modificado )
 
+
+
+
+DESFAZENDO AS COISAS 
+


Então eu posso dar um checkout e enfim.



git reset --hard 

pp918545@penguin:~/git-course$ git log
commit 39f9c513a24f5f65c150a73e811e030c535fca96 (HEAD -> master)
Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 18:29:41 2023 -0300

     ok

commit 770b83d73e7621d9e417b66b4e5732fe56cbcbda
Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 18:28:58 2023 -0300

Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 18:28:58 2023 -0300

     Comandos atualizados
     
     
 
git reset --hard 770b83d73e7621d9e417b66b4e5732fe56cbcbda

vai sumir o git " ok "

pp918545@penguin:~/git-course$ git log
commit 770b83d73e7621d9e417b66b4e5732fe56cbcbda
Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 18:28:58 2023 -0300

Author: Pedro Lucas <pp918545@gmail.com>
Date:   Thu Sep 7 18:28:58 2023 -0300

     Comandos atualizados

É bom usar ele, apenas quando nós ainda não jogamos esse git no repositório de uma nuvem
,para não causar confusão. 
