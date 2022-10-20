
# Human errors within formal verification
## X-Men: A Mutation-Based Approach for the Formal Analysis of Security Ceremonies
### D. Sempreboni and L. Viganò; 2020

```mermaid
flowchart TB
Tool --creates-->     Mutation_rules --to automatically<br/>generate-->Mutations --that influence--> Other_agents --who_may--> Not_reply_back -.- do_not_care
    Other_agents --who_may--> Reply_back --if--> Human_mutations --satisfy--> Matching_mutations -->|that| adjust_non_human_role-->|accordig|Human_mutations
    Tool --propagates--> Human_mutations 
```
## Modeling human errors in security protocols
### D. Basin, S. Radomirovic and L. Schmid; 2016

```mermaid
flowchart TB
Agent --if_follow_the_protocol--> Infallible_human
Untrained_human_rules --allow--> send_any_secret_to_anybody
send_any_secret_to_anybody --without further restrictions-->Untrained_human
Untrained_human --can perform-->  Any_action
send_any_secret_to_anybody --with--> A_set_of_rules 
A_set_of_rules --modeled using-->  Database_of_human_knowledge--became--> Rule_based_human
Infallible_human --with--> A_set_of_errors_he_can_commit --became--> Skilled_human
```
