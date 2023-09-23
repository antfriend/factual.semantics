# factual.semantics

The hidden shapes of intelligence, bridging the natural and the artificial in semantically symbolic entity relationship models. 


```mermaid
flowchart TD
    A(This) --> B(all this)
    A --> C(what does it mean?)

```
The Jupyter notebook example [auto_taxonomy](auto_taxonomy.ipynb) generates a language model and knowledge graph of a "mindfulness" article and the relevant UMLS concepts.  

Messing around with mermaid ...
```mermaid
erDiagram
    NOUNOID only one to zero or more CAR : is_a
    VERBOID only one to zero or more PERSON : is_a
    CAR ||--o{ NAMED-DRIVER : allows
    CAR {
        string registrationNumber PK
        string make
        string model
        string[] parts
    }
    PERSON ||--o{ NAMED-DRIVER : is
    PERSON {
        string driversLicense PK "The license #"
        string(99) firstName "Only 99 characters are allowed"
        string lastName
        string phone UK
        int age
    }
    NAMED-DRIVER {
        string carRegistrationNumber PK, FK
        string driverLicence PK, FK
    }

```