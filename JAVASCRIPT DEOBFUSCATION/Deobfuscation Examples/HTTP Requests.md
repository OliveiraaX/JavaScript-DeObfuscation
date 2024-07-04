# HTTP Requests


Na seção anterior, descobrimos que a função principal em `secret.js` está enviando uma solicitação POST vazia para `/serial.php`. Nesta seção, vamos tentar fazer o mesmo usando cURL para enviar uma solicitação POST para `/serial.php`. Para aprender mais sobre cURL e solicitações web, você pode conferir o módulo de Solicitações Web.

## cURL

cURL é uma ferramenta poderosa de linha de comando usada em distribuições Linux, macOS e também nas versões mais recentes do Windows PowerShell. Com ela, podemos solicitar qualquer site fornecendo sua URL e obteremos o texto no formato:

```bash
$ curl http://SERVER_IP:PORT/
html
Copiar código
<!DOCTYPE html>
<html>
<head>
    <title>Gerador de Série Secreta</title>
    <style>
        *,
        html {
            margin: 0;
            padding: 0;
            border: 0;
            /* ...SNIP... */
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Gerador de Série Secreta</h1>
        <p>Esta página gera séries secretas!</p>
    </div>
</body>
</html>
```
Este é o mesmo HTML que vimos ao verificar o código-fonte na primeira seção.

## Solicitação POST
Para enviar uma solicitação POST, precisamos adicionar a flag -X POST ao nosso comando, que indica que queremos enviar uma solicitação POST:

```
$ curl -s http://SERVER_IP:PORT/ -X POST
```
Adicionamos -s para reduzir a desordem na resposta, evitando dados desnecessários.

No entanto, solicitações POST geralmente contêm dados POST. Para enviar esses dados, usamos a flag -d "param1=amostra" para incluir nossos dados para cada parâmetro:


```
$ curl -s http://SERVER_IP:PORT/ -X POST -d "param1=amostra"
```
Agora que sabemos como usar cURL para enviar solicitações POST básicas, na próxima seção, vamos usar isso para replicar o que server.js está fazendo e entender melhor sua finalidade.