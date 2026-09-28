# Diagrama de classes — painel polimórfico

```mermaid
classDiagram
    class Sensor {
        <<abstract>>
        -tag : string
        +tag() string
        +valor() double*
        +unidade() string*
        +atualizar(leitura: double) bool*
        +emAlerta() bool*
    }

    class SensorNivel {
        -valor_ : double = 50.0
        +valor() double
        +unidade() string
        +atualizar(leitura) bool
        +emAlerta() bool
    }

    class SensorTemperatura {
        -valor_ : double = 25.0
        +valor() double
        +unidade() string
        +atualizar(leitura) bool
        +emAlerta() bool
    }

    class SensorPressao {
        -valor_ : double = 1.0
        +valor() double
        +unidade() string
        +atualizar(leitura) bool
        +emAlerta() bool
    }

    class Painel {
        +linhaPainel(const Sensor&) string
    }

    Sensor <|-- SensorNivel
    Sensor <|-- SensorTemperatura
    Sensor <|-- SensorPressao
    Painel ..> Sensor : usa referência (contrato)