Quando compilamos um código TS, ele por default converte o typescript para uma versão muito antiga do Javascript. A ES5. Isso acontece por questões de compatibilidade.

Para especificar uma versão do TypeScript ao tsc utilizamos o **--target**. EX:

``` bash
tsc --target es2015 hello.ts
```

