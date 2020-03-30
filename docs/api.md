## API - Endpoints

Default host = 0.0.0.0
<h3>GET: host/</h3>

* `ID` - Recebe como argumento do html (host/?ID<"numero">) -> Numero do desafio que voce esta checando

<h5>Respostas :</h5>
* `""Ainda não há desafios! Volte mais tarde."` - Quando ha tentativa de get e ainda nao foram colocados desafios para serem realizados
* `""Oops... Desafio invalido!""` - Quando o ID acessado nao tem um desafio relacionado.
* `"Sem Erros"` - Seu Post foi acetio.

<h3>Post: host/</h3>

* `ID` - Recebe como argumento do html (host/?ID<"numero">) -> Numero do desafio que voce esta enviando como resposta

<h5>Respostas :</h5>
* `"Sorry... Prazo expirado!"` - Quando realizado um post depois de terminado o prazo.
* `"Boa tentativa, mas não vai dar certo!"` - Tentou enviar a resposta em branco.
* `"Sem Erros"` - Seu Post foi acetio.

<h3>POST: host/pass</h3>

* `ID` - Envia o form da pagina como argumento do request.

<h5>Respostas :</h5>
* `"As novas senhas nao batem"` - Quando as novas senhas nao coincidem.
* `"A senha antiga nao confere"` - Erro de digito na senha que esta sendo trocada.
* `"Senha alterada com sucesso"` - Sucesso na troca de senhas.

<h3>host/logout</h3>

* URL para realizar o logout.
