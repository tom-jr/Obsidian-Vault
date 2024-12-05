**data** 22/11/2024
## Definição do Operador defaultIfEmpty
Para Mono ou Flux o operador irá devolver um valor para a emissão caso o fluxo reativo for vazio(Não há emissões a serem realizadas).

Exemplo prático:

```java 
Flux.empty()  
        .defaultIfEmpty("Hello World default if empty!")  
        .subscribe(Util.subscriber());
```
