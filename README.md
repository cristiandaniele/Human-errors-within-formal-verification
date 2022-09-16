
# X-Men: A Mutation-Based Approach for the Formal Analysis of Security Ceremonies

## D. Sempreboni, L. Viganò
### 1. Introduction
```mermaid
flowchart TB
Tool --creates-->     Mutation_rules --to automatically<br/>generate-->Mutations --that influence--> Other_agents --who_may--> Not_reply_back -.- do_not_care
    Other_agents --who_may--> Reply_back --if--> Human_mutations --satisfy--> Matching_mutations -->|that| adjust_non_human_role-->|accordig|Human_mutations
    Tool --propagates--> Human_mutations 
```

### 2. Case study: Main cerimony for the Tube

```mermaid
sequenceDiagram
    actor Human
    Human->>Gate In: Card
    Gate In ->> Human : (Card,Gate_In_ID)
    Human ->> Gate Out : (card,bal(card),Gate_In_ID)
    Note right of Gate Out: Gate Out charges<br>the right fare
    Gate Out ->> Human : (card,bal(card),finish)
    
```

### 3. The approach