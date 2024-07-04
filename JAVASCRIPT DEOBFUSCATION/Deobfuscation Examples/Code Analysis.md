# Análise de Código
Agora que deobfuscamos o código, podemos começar a analisá-lo:

javascript
```
'use strict';
function generateSerial() {
  ...SNIP...
  var xhr = new XMLHttpRequest;
  var url = "/serial.php";
  xhr.open("POST", url, true);
  xhr.send(null);
};
```
Vemos que o arquivo secret.js contém apenas uma função, generateSerial.

## Requisições HTTP
Vamos examinar cada linha da função generateSerial.

## Variáveis de Código
A função começa definindo uma variável *xhr*, que cria um objeto *XMLHttpRequest*. Como talvez não saibamos exatamente o que *XMLHttpRequest* faz em JavaScript, vamos pesquisar sobre *XMLHttpRequest* para entender seu uso.

Após a leitura, vemos que é uma função JavaScript que lida com requisições web.

A segunda variável definida é a variável url, que contém um URL para */serial.php*, que deve estar no mesmo domínio, já que nenhum domínio foi especificado.

## Funções de Código
Em seguida, vemos que *xhr.open* é usado com "POST" e *url*. Podemos pesquisar novamente esta função e vemos que ela abre a requisição HTTP definida como "POST" para o URL, e então a próxima linha *xhr.send* enviará a requisição.

Portanto, tudo que *generateSerial* está fazendo é simplesmente enviar uma requisição POST para */serial.php*, sem incluir nenhum dado POST ou recuperar qualquer coisa em retorno.

Os desenvolvedores podem ter implementado esta função para quando precisarem gerar um serial, como ao clicar em um certo botão de "Gerar Serial", por exemplo. No entanto, como não vimos nenhum elemento HTML semelhante que gere seriais, os desenvolvedores podem não ter usado esta função ainda e a mantiveram para uso futuro.

Com o uso de deobfuscação de código e análise de código, conseguimos descobrir esta função. Agora podemos tentar replicar sua funcionalidade para ver se ela é tratada no servidor ao enviar uma requisição POST. Se a função estiver habilitada e tratada no lado do servidor, podemos descobrir uma funcionalidade não lançada, que geralmente tende a ter bugs e vulnerabilidades.