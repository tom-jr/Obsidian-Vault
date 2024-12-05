SwitchIfEmpty é um operador que semelhante ao [[defaultIfEmpty]]. Com diferença no objeto ao que ele emite. No switchIfEmpty emitimos um novo Flux/Mono quando as emissões forem vazias. 
Podemos lançar um Flux ou Mono quando for um flux. Mas quando for Mono podemos lançar outro Mono apenas.
Ex:

``` java
Flux.empty()  
        .switchIfEmpty(Flux.just("Hello","World"))  
        .subscribe(Util.subscriber());
```
