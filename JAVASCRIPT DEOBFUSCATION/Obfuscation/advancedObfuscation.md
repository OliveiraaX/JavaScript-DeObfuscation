# Ofuscação Avançada

Até agora, conseguimos tornar nosso código obfuscado e mais difícil de ler. No entanto, o código ainda contém strings em texto claro, o que pode revelar sua funcionalidade original. Nesta seção, vamos experimentar algumas ferramentas que devem completamente ofuscar o código e ocultar qualquer vestígio de sua funcionalidade original.

## Obfuscador

Vamos visitar [obfuscator.io](https://obfuscator.io). Antes de clicarmos em "obfuscate", vamos alterar a codificação do Array de Strings para Base64.

Agora, podemos colar nosso código e clicar em "obfuscate":

Obtemos o seguinte código:

```javascript
var _0x1ec6=['Bg9N','sfrciePHDMfty3jPChqGrgvVyMz1C2nHDgLVBIbnB2r1Bgu='];(function(_0x13249d,_0x1ec6e5){var _0x14f83b=function(_0x3f720f){while(--_0x3f720f){_0x13249d['push'](_0x13249d['shift']());}};_0x14f83b(++_0x1ec6e5);}(_0x1ec6,0xb4));var _0x14f8=function(_0x13249d,_0x1ec6e5){_0x13249d=_0x13249d-0x0;var _0x14f83b=_0x1ec6[_0x13249d];if(_0x14f8['eOTqeL']===undefined){var _0x3f720f=function(_0x32fbfd){var _0x523045='abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789+/=',_0x4f8a49=String(_0x32fbfd)['replace'](/=+$/,'');var _0x1171d4='';for(var _0x44920a=0x0,_0x2a30c5,_0x443b2f,_0xcdf142=0x0;_0x443b2f=_0x4f8a49['charAt'](_0xcdf142++);~_0x443b2f&&(_0x2a30c5=_0x44920a%0x4?_0x2a30c5*0x40+_0x443b2f:_0x443b2f,_0x44920a++%0x4)?_0x1171d4+=String['fromCharCode'](0xff&_0x2a30c5>>(-0x2*_0x44920a&0x6)):0x0){_0x443b2f=_0x523045['indexOf'](_0x443b2f);}return _0x1171d4;};_0x14f8['oZlYBE']=function(_0x8f2071){var _0x49af5e=_0x3f720f(_0x8f2071);var _0x52e65f=[];for(var _0x1ed1cf=0x0,_0x79942e=_0x49af5e['length'];_0x1ed1cf<_0x79942e;_0x1ed1cf++){_0x52e65f+='%'+('00'+_0x49af5e['charCodeAt'](_0x1ed1cf)['toString'](0x10))['slice'](-0x2);}return decodeURIComponent(_0x52e65f);},_0x14f8['qHtbNC']={},_0x14f8['eOTqeL']=!![];}var _0x20247c=_0x14f8['qHtbNC'][_0x13249d];return _0x20247c===undefined?(_0x14f83b=_0x14f8['oZlYBE'](_0x14f83b),_0x14f8['qHtbNC'][_0x13249d]=_0x14f83b):_0x14f83b=_0x20247c,_0x14f83b;};console[_0x14f8('0x0')](_0x14f8('0x1'));
```
Este código está claramente mais obfuscado e não podemos ver mais nenhum vestígio do nosso código original. Agora podemos tentar executá-lo em *JSConsole* para verificar se ainda executa sua função original. Experimente ajustar as configurações de obfuscação em obfuscator.io para gerar um código ainda mais obfuscado e, em seguida, teste novamente em JSConsole para verificar se ainda funciona conforme esperado.

## Mais Obfuscação
Agora, devemos ter uma ideia clara de como a obfuscação de código funciona. Ainda existem muitas variações de ferramentas de obfuscação de código, cada uma obfuscando o código de maneira diferente. Tome o seguinte código JavaScript como exemplo:

javascript
```
[][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+!+[]]][([][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+!+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+!+[]]])[+!+[]+[+[]]]+([][[]]+[])[+!+[]]+(![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[+!+[]]+([][[]]+[])[+[]]+([][(![]]+(!![]+[][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+!+[]]])[+!+[]+[+[]]]+(!![]+[])[+!+[]]])[!+[]+!+[]+[+[]]]](!+[]+!+[]+[+[]])))()....
```
Podemos executar este código e ele ainda realizará sua função original:

https://jsconsole.com/

Nota: O código acima foi cortado porque é muito longo, mas o código completo deverá rodar com sucesso.

Podemos tentar ofuscar o código usando a mesma ferramenta no JSF e, em seguida, testá-lo novamente. Vamos observar que o código pode levar algum tempo para ser executado, o que mostra como a obfuscação de código pode afetar o desempenho, como mencionado anteriormente.

Existem muitos outros obfuscadores de JavaScript, como JJ Encode ou AA Encode. No entanto, esses obfuscadores geralmente tornam a execução/compilação do código muito lenta, então não é recomendado usá-los a menos que seja por um motivo óbvio, como contornar filtros ou restrições da web.
