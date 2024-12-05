**data** 22/11/2024
**Fonte** Curso Reactive Programming in Java

## O que é o operador onErroContinue?
Podemos lançar a exception e continuar as emissões dos valores do Fluxo reativo.
O onErrorContinue não para a emissão quando lançado o erro. Ele nos da a oportunidade de criarmos um statement que manipula o erro e objeto da emissão

exemplo:
```java
Flux.range(1, 10) {
map(i -> i == ? i / 0 : i)
.onErrorContinue((ex, obj) ->  log.error("==> {}", obj, ex))
.subscribe(Util.subscribe());
}
```