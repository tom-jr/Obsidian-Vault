O que é o AssertThat?
um método do [[AssertJ]] que faz asserção em um método. Ex:

``` java
@Test  
public void calculatorTest(){  
    Calculadora calculadora = new Calculadora();  
    Assertions.assertThat(calculadora.somar(2,4)).isEqualTo(6);  
}
```

Nesse statement é feito uma asserção onde é verificado se o retorno do método somar é igual a 6. Caso for o Teste é bem sucedido 