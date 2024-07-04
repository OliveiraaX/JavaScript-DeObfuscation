# Ofuscação de Código

## O que é Ofuscação

Ofuscação é uma técnica usada para tornar um script mais difícil de ler por humanos, mas ainda funcional. Isso é feito automaticamente por ferramentas de ofuscação que reescrevem o código de forma complicada, o que pode afetar um pouco o desempenho.

### Exemplo de Ofuscação

Ofuscadores de código transformam o código em algo parecido com um quebra-cabeça, onde cada palavra e símbolo é substituído por outra coisa. Isso é especialmente comum em JavaScript, que é enviado ao navegador e executado em texto simples.

[Veja um exemplo de ofuscação de JavaScript](http://beautifytools.com/javascript-obfuscator.php).

### Linguagens Comuns

Linguagens como Python e PHP geralmente rodam no servidor e ficam ocultas dos usuários. Já o JavaScript é executado no navegador do usuário, o que torna a ofuscação mais comum.

## Casos de Uso

### Proteção de Propriedade Intelectual

Desenvolvedores ofuscam o código para esconder a lógica e evitar que ele seja copiado ou reutilizado sem permissão. Isso torna a engenharia reversa mais difícil.

### Segurança

Ofuscação pode adicionar uma camada de segurança, dificultando a identificação de vulnerabilidades. No entanto, não é recomendado fazer autenticação ou criptografia no lado do cliente, pois é mais fácil de atacar.

### Ações Maliciosas

Invasores usam ofuscação para esconder scripts maliciosos e evitar a detecção por sistemas de segurança.

## Exemplo Prático

Vamos aprender a ofuscar um código JavaScript simples e ver como ele funciona antes e depois da ofuscação.

### Passo a Passo

1. **Código Original**:
    ```javascript
    function saudacao() {
        alert("Olá, mundo!");
    }
    saudacao();
    ```

2. **Ofuscar o Código**:
    - Use uma ferramenta online de ofuscação, como [JavaScript Obfuscator](http://beautifytools.com/javascript-obfuscator.php).
    - Cole o código original e clique em "Obfuscate".

3. **Código Ofuscado**:
    ```javascript
    eval(function(p,a,c,k,e,d){e=function(c){return c.toString(36)};if(!''.replace(/^/,String)){while(c--)d[c.toString(a)]=k[c]||c.toString(a);k=[function(e){return d[e]}];e=function(){return'\\w+'};c=1};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p}('2 0(){1("4, 3!")}0();',5,5,'saudacao|alert|function|mundo|Olá'.split('|'),0,{}))
    ```

4. **Executar o Código**:
    - Compare o comportamento do código original com o código ofuscado.
    - Ambos devem exibir o alerta "Olá, mundo!".

### Conclusão

Ofuscação é uma técnica útil para proteger o código, mas tem suas limitações e não deve ser usada como única medida de segurança. Entender como funciona ajuda a desofuscar quando necessário.
