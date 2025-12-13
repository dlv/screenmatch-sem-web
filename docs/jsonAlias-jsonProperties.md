# Para saber mais: JsonAlias e JsonProperty

## Introdução:
A aula explora as anotações @JsonAlias e @JsonProperty da biblioteca Jackson, utilizadas para mapear propriedades de classes Java para campos JSON.

### @JsonProperty:

- Usada para definir o nome exato da propriedade JSON associada a um campo Java.
- Útil quando o nome no JSON deve ser diferente do nome do campo Java.

#### Exemplo:
```java
    public class Pessoa {
        @JsonProperty("nome")
        private String nomeCompleto;
    }
```

### @JsonAlias:

- Usada para definir um ou mais apelidos para o nome da propriedade JSON.
- Permite que a biblioteca encontre o valor JSON correspondente, mesmo que o nome da propriedade no JSON não corresponda exatamente ao nome do campo Java.
- Útil para lidar com diferentes versões de um JSON ou permitir múltiplos nomes para uma propriedade.

#### Exemplo:

```java
    public class Pessoa {
        @JsonAlias({"nomeCompleto", "nome"})
        private String nomeCompleto;
    }
```

## Documentação:

Para mais informações, consulte a [Documentação do Jackson Annotations](https://github.com/FasterXML/jackson).