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
 
 
 
 
 
