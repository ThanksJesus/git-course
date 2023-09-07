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

