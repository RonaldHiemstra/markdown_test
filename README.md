# Demo markdown with some diagrams

## PlantUML

### Class diagram

```plantuml
@startuml
class Animal {
    + age: int
    + gender String
    + isMammal()
    + mate()
}
Animal <|-- Duck
Animal <|-- Fish
Animal <|-- Zebra

class Duck{
    +String beakColor
    +swim()
    +quack()
}
class Fish{
    -int sizeInFeet
    -canEat()
}
class Zebra{
    +bool is_wild
    +run()
}
class Animal
note left: Aren't we all the same?
@enduml
```

## Sequence diagram

```plantuml
@startuml sequence register

actor Alice
box "all my friends <:wink:>" #LightBlue
Alice->John: Hello John, how are you?
actor Bob
John-->Alice: Great!
Alice->>John: See you later!
end box
@enduml
```

## [Mermaid](https://mermaid-js.github.io/mermaid/#/)

Mermaid does not (yet) support all the PlantUML type of diagrams. [But they are working on it...](https://github.com/mermaid-js/mermaid/issues/177)

### Class diagram

```mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
```

### Sequence diagram

```mermaid
sequenceDiagram
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!
    Alice-)John: See you later!
```
