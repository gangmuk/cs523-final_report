# Template of Finall Course Project Report

The repo includes a makefile so you can directly `make` the PDF. 

# Structure of the paper

## Contents
- Common patterns of failure cases
- Describing each failure cases
- Describing why they happen
  - System design level explanation
    - Reconciliation
    - There is no  like system 
    - Many controllers interact each other
  - Development environment explanation
    - Open source, different contributors implement different part and they are likely to be conflicted each other
  - Challenges
    - Why is it challenging to find failures?
      - Big system
      - Hard to test or verify it since the search space is enormously large.
    - Why is it challenging to fix failures?
      - If you look at each controller separately, individual controller does not imply any buggy or unexpected behavior. However, once it interacts with other parts of the system, they are entangled each other and break down. If controller is tested individually, it will pass all the tests. Undesirable behaviro
      - Most of time, it is hard to argue that they are bugs. What is worse is even if it is agreed by the community that it is a bug, oftentimes there is no clear way to fix it. Again, this is because individual controller is not committing misconduct. It makes 
- Insights from failure study
