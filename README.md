# Table of contents
1. [Purpose](#purpose)
2. [GitHub](#github)
3. [Schema](#schema)
    1. [Database Layers](#schema_layers)
    2. [The Layers' Tables](#schema_tables)
    3. [Variable Definitions](#schema_definitions)
4. [Access](#access)


## Purpose <a name="purpose"></a>

This repository hosts the code and documentation associated with the SAFE historical firm database for Germany. It further provides information on how to formally [access the database](#access).

## GitHub Structure <a name="github"></a>
Note that the repository relies on GitHub submodules. Submodules can either be external stand-alone projects or repositories established only for creating the SAFE database. Moreover, running the file 

><span style="background-color:#ddd">main.py</span>.

builds all layers of the database, including descriptive statistics and graphical illustrations of the layers, from scratch. The Graph below illustrates the logic of the process. Each gray rectangular represents a submodule.

```mermaid
flowchart TD
    subgraph 1["Input Layer"]
        direction BT
        subgraph 1.1["Raw Data Access"]
            direction LR
            UBM["UB Mannheim"] --> SAFE["SAFE DB"]
        end
        subgraph 1.2["Enrichment"]
            direction LR
            i2 -->f2
        end
    end
    subgraph 2["Original Layer"]
        direction LR
        subgraph 2.1["Line Classification"]
            direction TB
            Tab["Tagging"] --> Train["Model<br/>Training"] --> Pred["Prediction"]
        end
        subgraph 2.2["Industry Identification"]
            direction LR
            C --> D
        end
        subgraph 2.3["Firm Identification"]
            direction LR
            E --> F
        end
        subgraph 2.4["Item Identification"]
            direction LR
            G --> H
        end
        subgraph 2.5["Parsing"]
            direction LR
            2.5.1["Line<br/>Combination"] --> 2.5.2["Variable<br/>Extraction"]
        end
        2.1 --> 2.2
        2.2 --> 2.3
        2.3 --> 2.4
        %%
        2.2 --> 2.5
        2.3 --> 2.5
        2.4 --> 2.5
    end
    subgraph 3["Linking"]
        direction TB
        Tab2["Tagging"] --> Train2["Model<br/>Training"] --> Pred2["Prediction"]
    end
    subgraph 4["Graphical Illustrations"]
        direction BT
        subgraph 4.1
            direction LR
            X --> Y
        end
    end
    %%arrows between subgraphs
    1 --> 2
    2 --> 3
    3 --> 4
```

## Data Model / Database Design <a name="schema"></a>

### Database Layers <a name="schema_layers"></a>

embed graph here

### The Layers' Tables <a name="schema_tables"></a>

embed graphs here

### Variable Definitions <a name="schema_definitions"></a>

## Access <a name="access"></a>

Please contact [Dennis Gram](mailto:gram@safe-frankfurt.de), the head of the SAFE data center, for access
