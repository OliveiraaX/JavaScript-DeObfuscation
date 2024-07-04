# Ofuscação de Código

## Executando Código JavaScript

Vamos usar a seguinte linha de código JavaScript como exemplo e tentar ofuscá-la:

```javascript
console.log('Deobfuscation Module');
```
## Testando o Código Original

Primeiro, vamos testar o código original em texto claro para ver seu funcionamento. Acesse https://jsconsole.com/, cole o código e pressione Enter. Você verá a saída:

## JavaScript Deobfuscation Module
Isso é feito usando a função console.log().

## Minificando Código JavaScript
Uma forma comum de reduzir a legibilidade do código JavaScript, mantendo-o funcional, é a minificação. A minificação coloca todo o código em uma única linha, o que é mais útil para códigos longos.

Ferramentas como https://www.toptal.com/developers/javascript-minifier podem ajudar a minificar o código. 

## Testando o Código Minificado
Copie o código minificado de volta para JSConsole e execute-o para ver que ainda funciona conforme o esperado. Normalmente, o código minificado é salvo com a extensão .min.js.

## Ofuscando Código JavaScript
Agora, vamos ofuscar nossa linha de código para torná-la mais obscura e difícil de ler. Use BeautifyTools para ofuscar o código.

javascript
```
eval(function(p,a,c,k,e,d){e=function(c){return c};if(!''.replace(/^/,String)){while(c--){d[c]=k[c]||c}k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1};while(c--){if(k[c]){p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c])}}return p}('5.4(\'3 2 1 0\');',6,6,'Module|Deobfuscation|JavaScript|HTB|log|console'.split('|'),0,{}))
```
## Testando o Código Ofuscado
Copie o código ofuscado para *JSConsole* para verificar se ainda executa a mesma função. Você verá a mesma saída:
```
JavaScript Deobfuscation Module
Tipos de Ofuscação
Ofuscação de Pacotes (Packing)
A ofuscação de pacotes geralmente envolve converter todas as palavras e símbolos do código em uma lista ou dicionário e referenciá-los usando uma função como function(p,a,c,k,e,d) para reconstruir o código original durante a execução. Essa técnica reduz a legibilidade do código, mas pode deixar algumas strings principais visíveis em texto claro.
```

## Tipos de Ofuscação
Ofuscação de Pacotes (Packing)
A ofuscação de pacotes geralmente envolve converter todas as palavras e símbolos do código em uma lista ou dicionário e referenciá-los usando uma função como function(p,a,c,k,e,d) para reconstruir o código original durante a execução. Essa técnica reduz a legibilidade do código, mas pode deixar algumas strings principais visíveis em texto claro.
