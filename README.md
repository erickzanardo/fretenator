# Fretenator
Client java para cálculo do frete usando o webservice dos correios

# Maven

```xml
 <repository>
    <id>erickzanardo-releases</id>
    <url>http://erickzanardo.github.com/maven/releases/</url>
  </repository>

  <dependency>
    <groupId>org.eck.correiostools</groupId>
    <artifactId>fretenator</artifactId>
    <version>1.0</version>
  </dependency>
```

# Como usar

```java
Fretenator fretenator = new Fretenator();
fretenator.codServico("41106");
fretenator.codFormato(1);
fretenator.altura(11d);
fretenator.largura(12d);
fretenator.comprimento(16d);
fretenator.peso("0,450");
fretenator.cepOrigem("11111111");
fretenator.cepDestino("11111111");
FretenatorResult result = fretenator.result();
FretenatorResultItem servico = result.getServico(41106);

System.out.println(servico.getErro());
System.out.println(servico.getMensagemDeErro());
System.out.println(servico.getPrazo());
System.out.println(servico.getValor());
System.out.println(servico.getEntregaDomiciliar());
System.out.println(servico.getEntregaSabado());
```

Utilize este [documento](http://www.correios.com.br/para-voce/correios-de-a-a-z/pdf/calculador-remoto-de-precos-e-prazos/manual-de-implementacao-do-calculo-remoto-de-precos-e-prazos) (pág 10) para explicação dos parâmetros, códigos e etc
