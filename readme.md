# Object data manipulation

O portfólio apresenta técnicas avançadas de manipulação de dados de objetos em JavaScript, destacando o uso de modelos marcados para localização e destaque de palavras-chave, bem como a adição de números de linha em strings multilinha.

### Quasi-tagged templates

Você está trabalhando em uma biblioteca de localização que usa modelos marcados para lidar com vários idiomas. A função chamada localize que atua como um modelo quase marcado. A função deve receber uma string de modelo e um objeto contendo traduções específicas do idioma. Deve substituir os espaços reservados na string do modelo pelas traduções correspondentes do objeto fornecido.

```javascript
const language = "en";
const greeting = "greet";
const introduction = "intro";

const localizedGreeting = localize`${language}, ${greeting}`;
const localizedIntroduction = localize`${language}, ${introduction}`;

console.log(`${localizedGreeting}, ${localizedIntroduction}`);
```

### Advanced tagged templates

A função chamada highlightKeywords que atua como um modelo marcado e deve receber uma string de modelo e um array de palavras-chave.
Ele deve destacar cada ocorrência de uma palavra-chave no modelo envolvendo-a em um elemento <span> com uma classe CSS específica.

```javascript
const keywords = ["JavaScript", "template", "tagged"];
const template = highlightKeywords`Learn ${keywords[0]} tagged templates to create custom ${keywords[1]} literals for ${keywords[2]} manipulation.`;

console.log(template);
```

### Multiline tagged template

Função chamada multiline que pega uma string de modelo e retorna uma string com números de linha adicionados no início de cada linha.Os números das linhas devem começar em 1 e aumentar para cada linha, preservando o recuo original de cada linha.

```javascript
const code = multiline`
function add(a, b) {
  return a + b;
}
`;

console.log(code);
```
