# factual.semantics

The hidden shapes of intelligence, bridging the natural and the artificial in semantically symbolic entity relationship models. 

```mermaid
flowchart TD
A(This) --> B(all this)
A --> C(what does it mean?)
```

The Jupyter notebook example >>>  [auto_taxonomy](auto_taxonomy.ipynb) <<< generates a minimal language model and knowledge graph of a "mindfulness" article and the relevant UMLS concepts.  Semantic alignment separates the meaningful concepts from the noise in entity recognition. The resulting data is diagramed like so: 


```mermaid
erDiagram
    PUBMED_CONTENT only one to zero or more PUBMED : contains
    UMLS_CONCEPTS only one to zero or more CUIs : contains
    PUBMED ||--o{ SEMANTIC-FOCUS : has-semantic-focus
    PUBMED {
        string id "28031068"
        string title "What defines mindfulness-based programs? The warp and the weft."
        string abstract "There has been an explosion of interest in mindfulness-based programs (MBPs) such as Mindfulness-Based Stress Reduction (MBSR) and Mindfulness-Based Cognitive Therapy."
    }
    CUIs ||--o{ SEMANTIC-FOCUS : applies-to
    CUIs {
        menp C3542996 "Mindfulness"
        menp C0086045 "Mental concentration"
        topp C0009244 "Cognitive Therapy" 
        topp C4527300 "Meditation-Based Stress Reduction Program"
        menp C2985553 "Mindfulness Relaxation"

    }
    SEMANTIC-FOCUS {
        menp Mental_Process 
        topp Therapeutic_or_Preventive_Procedure
    }

```