# Tutorial para Desenvolvimento

## Configurando ambiente de desenvolvimento

Priemiramente e necessaria sqlite3 
Sistemas baseados em debian (Ubuntu, Debian etc.):   

    $ sudo apt-get update
    $ sudo apt-get install sqlite3

Sistemas baseado em RPM (RHEL, CentOS, Fedora etc.):

    $ sudo yum update
    $ sudo yum install sqlite

Tambem e necessaria a instalacao do flask e o flask_httpauth com:

    $ sudo pip3 install flask
    $ sudo pip3 install flask_httpauth


## Instalacao do software

Para a instalacao do software e necessario entrar no ambiente do sqlite3 para criar o banco de dados utilizando

    $ sqlite3 quiz.db

Uma vez no ambiente do sqlite3 rode o script de criacao do banco de dadods com 

    $ .read quiz.sql

Com o banco de dados criados e necessario criar agora os usuarios. Crie um arquivo chamado  ```users.csv ```  e siga as instrucoes de criacao de usuario na aba professores.

Com isso o software esta pronto. Para rodar basta executar:

    $ python3 softdes.py


## Estrutura do codigo

As funcoes que constituem o codigo sao:

* lambda_handler(event):Recebe as informacoes de um envio, realiza o teste e retorna o feedback


* converte_data(orig): Muda a ordem de chunks de uma string de entrada


* get_quizes(user): Resgata os todos os quizes de um usuario


* get_user_quiz(userid, quizid): Resgata um quiz expecifico de um usuario na tabela USERQUIZ


* set_user_quiz(userid, quizid, sent, answer, result): Designa um quiz para um aluno com sua resposta e outras informacoes


* get_quiz(id_q, user): Resgata um quiz expecifico de um usuario na tabela QUIZ


* set_info(pwd, user): Designa as credenciais a um usuario


* get_info(user): Resgata as crendenciais de um usuario


* get_password(username): Resgata a senha de um usuario


* hash_pw(password): Faz o Hash da senha para armazenagem

