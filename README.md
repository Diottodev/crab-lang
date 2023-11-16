# Crab-lang

### Este é um projeto que consiste na criação de uma linguagem de programação chamada crab-lang e um compilador escrito em Rust que converte código crab-lang para JavaScript.

# Sobre crab-lang

crab-lang é uma linguagem de programação simples projetada para facilitar a aprendizagem e compreensão de conceitos básicos de programação. Ela suporta declarações de variáveis, atribuições, literais de string, literais inteiros e uma função de impressão `log` para facilitar a depuração.

A linguagem `crab-lang` possui uma sintaxe básica com suporte para as seguintes construções:

- Declarações de variáveis: `var` e `var let` para variáveis mutáveis e imutáveis, respectivamente.
- Atribuições: Utiliza o operador `=` para atribuir valores a variáveis.
- Literais de string: Delimitados por aspas duplas `"` para representar cadeias de caracteres.
- Literais inteiros: Representados por sequências de dígitos.
- Função `log`: A palavra-chave log é usada para imprimir valores no console.

### Exemplo de código crab-lang:

```crab
var message = "Hello, crab-lang!";
log(message);
```

# Compilador em Rust

O compilador em Rust consiste em três partes principais:

## 1. Lexer (lexer):

Responsável por tokenizar o código-fonte crab-lang.
Identifica palavras-chave, identificadores, literais de string, literais inteiros e símbolos especiais.

## 2. Parser (parser):

Converte os tokens gerados pelo lexer em uma Árvore Sintática Abstrata (AST).
Reconhece declarações de variáveis e chamadas de função, especialmente a função log.

## 3. Gerador de Código (generate_js):

Utiliza a AST para gerar código JavaScript equivalente.
Lida com declarações de variáveis, diferencia entre let e const, e gera código JavaScript apropriado.
Para chamadas da função log, utiliza literais de modelo para interpolação de string.

# Como Usar

### Instalação do Rust:

Certifique-se de ter o Rust instalado em sua máquina. Você pode obtê-lo em https://www.rust-lang.org/tools/install.
Compilação e Execução:

### Clone este repositório: git clone https://github.com/seu-usuario/crab-lang-compiler.git

Navegue até o diretório do projeto: cd crab-lang-compiler

Compile o código Rust: `

```cmd
cargo build --release
```

Execute o compilador:

```cmd
cargo run ./target/release/crab-lang-compiler
```

Entrada e Saída:

Coloque seu código crab-lang em um arquivo, por exemplo, input.cr.

Execute o compilador:

```cmd
cargo run ./target/release/crab-lang-compiler input.cr
```

O código JavaScript gerado estará em um arquivo chamado output.js.

### Exemplo de Uso

Suponha que você tenha o seguinte código crab-lang em input.cr:

```crab
var message = "Hello, crab-lang!";
log(message);
```

Após executar o compilador, o código JavaScript resultante será:

```javascript
const message = "Hello, crab-lang!";
console.log(`{message}`);
```

### Este projeto é um ponto de partida para quem deseja entender como criar uma linguagem de programação simples e um compilador para traduzir código fonte para outra linguagem. Sinta-se à vontade para expandir e aprimorar a `crab-lang` e o compilador de acordo com suas necessidades.
