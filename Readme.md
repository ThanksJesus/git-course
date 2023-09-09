Um repositório simples, para o entedimento de como começar a usar o git na sua máquina
implementando a conexão SSH e a do seu repositório local para o GitHub .


Instale o Git ( https://git-scm.com/downloads )


Crie um repositório :

git config --global user.name "qualquer_nome" 

git config --global user.email "seu_email" 

git config --global core.editor editor_que_você_usa 


(leia os comandos_git.md)

------------------------------------------------------------------


Para fazer a config. SSH ( Conectar o Rep.local com o GitHub )


1- Abra Terminal.

2- Cole o texto abaixo, substituindo o endereço de e-mail pelo seu GitHub.

ssh-keygen -t ed25519 -C "your_email@example.com"

Observação: se estiver usando um sistema herdado que não dá suporte ao algoritmo Ed25519, use:

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"


Digite :


ls

cd nome_da_nova_pasta

.

/* Irá sugir duas pastas, uma com o nome: id_ssh  e a outra :id_ssh.pub */

.


Abra o arquivo, com :

cat id_ssh.pub

vi id_ssh.pub

ou o seu editor de código ;

.

Copie a chave SSH . E vá para o seu GitHub.

-----------------------------------------------------------------


No GitHub :

Vá em " Seetings "

SSH and GPG keys 

New SSH key

No Title ( Coloque o for do agrado, ou o que ira ajudar na hora de saber qual é o seu rep. pessoal ou do trabalho )

Na Key ( Cole a chave que você copiou do id_ssh.pub

Depois clique em Add SSH key



------------------------------------------------------------------


Para fazer a conexão do Repo.local com o GitHub .:






 
