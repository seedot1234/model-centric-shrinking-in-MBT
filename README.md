#  A model-centric approach to test case shrinking: utilising k-shortest path in model-based testing
This repo contains the raw data of the shrinking experiments of my thesis.

To evaluate the effectiveness of the proposed shrinking algorithms and validate their results, we integrated them into an existing shrinking interface developed by Lars Meijer. This interface is a research artefact built on top a commercial MBT suite; the Axini Modeling Platform. We conducted three controlled experiments (smartdoor, Koopman, and ATM), for which we developed multiple SUTs in Ruby and added their corresponding models to the MBT suite. The suite was then used to generate test cases for these systems. The shrinking interface was subsequently employed to reduce these test cases using both the proposed model-centric shrinkers and traditional trace-centric shrinkers.
## Files
- **data**: contains the raw shrinking data of the three experiments.
- **models**: contains the AML models of the Koopman and ATM experiments.
