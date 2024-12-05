NO_ANKI
É interessante copiar a estrutura de package do src do Spring para se situar melhor em navegar entre os testes automatizado.

Devemos definir o que é Unidade em nosso sistema. No caso do curso uma classe está sendo definida como uma **unidade**.

Criamos uma class nos packages de test com o mesmo nome da unidade com sufixo de **Test**. Ex para uma unidade chamada PlanetService:

``` java
public void PlanetServiceTest {

}
```

Podemos criar então nosso primeiro método de testa da unidade **PlanetServiceTest**. Vamos utilizar um padrão para nome do teste:

	opearacao_estado_retorno

``` java
public void PlanetServiceTest {
@Test
public void createPlanet_HappyFlux_ReturnsPlanet() {}
}
```
O @Test mapeia para o Spring que se trata de um método de teste e aplica as lógicas necessárias.

Vamos adicionar a unidade a ser testada, injetando-a na class teste. Vamos usar o contexto do Spring para gerenciar as injeções de dependência utilizando a annotation @SpringBootTest(classes = PlanetService.class). 
Passamos o PlanetService.class como argumento para o Spring não subir todo o contexto da aplicação atoa. Assim tornando o processo mais leve/rápido. Fica assim

``` java
@SpringBootTeste(classes = PlanetService.class)
public void PlanetServiceTest {

private final PlanetService planetService;  
  
public PlanetServiceTest(PlanetService planetService) {  
    this.planetService = planetService;  
	}
@Test
public void createPlanet_HappyFlux_ReturnsPlanet() {
	this.planetService.create(planet);
	}
}
```

Precisamos de um objeto Planet para salvar no create. Usaremos constantes. Criando um package common, podemos salvar constantes de objetos nela onde guardamos varias construções de objetos para reaproveitarmos