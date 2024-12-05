O Typescript tem um verificador de tipagem estática . Sistemas de tipo estáticos descrevem os formatos e comportamentos que os valores terão quando os executarmos. O typescript usa essas informações para nos alerta  que algo esta saindo dos trilhos.

``` typescript
const message = 'Hello!';
message();
```

	This expression is not calleble.
	Type 'String' has no call signatures.

Rodar esse statement nos dará uma mensagem de erro antes de executar o código.

## tsc, compilador TypeScript

Para compilar código TS em Javascript nos usamos o comando tsc do compilador TypeScript.
Criamos 1 arquivo hello.ts

``` typescript 
console.log('Hello World!');
```

depois no terminal rodamos o comando:

``` bash
tsc hello.ts
```
	 Lembrando que o typescript deve ter sido baixado previamente pelo package manage

