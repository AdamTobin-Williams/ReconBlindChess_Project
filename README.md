# ReconBlindChess_Project
This is a submission into the Reconnaissance Blind Chess competition held by the Johns Hopkins Applied Physics Laboratory from the participants Jeremiah Fan, Amaiyah Johnson, Adam Tobin-Williams, and Nico Valle

Competition: https://rbc.jhuapl.edu/challenge

Library: https://reconchess.readthedocs.io/en/latest/

Slides: https://circuitinstitute.slack.com/files/U010M1CAJ0M/F05G76Z8AJD/bytes_challenge_chess_2023.docx?origin_team=T89L0S73J&origin_channel=C05GPT9DNF4

proposed team name: Chessdinger

## Notes <br>
Piece Tracking
- The computer tracks all possible locations of opponent pieces and displays them in a semi-transparent overlay. This overrides the display mode as longs as tracking is active. If the number of possible boards exceeds 5,000 at the end of your turn, the assistant turns off. The Bot should be able to do this (or something similar)

Things the Bot will have to Consider
-  The most logical moves the opponent could have made (if the bot failed to sense what move was made)
-  Where the opponent’s piece moved FROM as well as moved to
-  Where the opponent most likely sensed
-  What would the most logical move be in regular chess?

Other Ideas
-  Is there a way to calculate the bot’s Elo? Would this be helpful at all?

What happens if we guess wrong?
- Backtrack and reevaluate?
- Continue?
   
## Bot Components <br>
- Possible Board State Tracker
  - Marks most likely states that can then be further analyzed
- Board Evaluation
  - Classical elements: Postiion, board control, material)
  - RBC Elements: uncertainty, potential for attack, potential for unknown check
- Sense Strategy
  - Reducing the number of possible states
  - Most informative for potential attacks/king safety
- _Guessing Opponent Sense_
  - Can help set up for better attacks
- Move Strategy
  - Searching through possibilities and selecting a move that best responds to the most likely board states
  - Should more heavily weigh factors like king safety/future check potential
 
 
## Resources <br>
Bots
- [Collection of Basic Bots](https://github.com/wrbernardoni/Baseline-Bots)
- [Strangefish, the winning bot of the 2019 NeurIPS tournament](/https://github.com/ginop/reconchess-strangefish)

Important Papers
- [RBC Overview and potential approaches to strategy](https://www.spiedigitallibrary.org/conference-proceedings-of-spie/9842/1/Reconnaissance-blind-multi-chess--an-experimentation-platform-for-ISR/10.1117/12.2228127.full?SSO=1)
- [Game state tracker](https://dl.acm.org/doi/pdf/10.5555/3417639.3417653)
- [Complexity and uncertainty in RBC](https://arxiv.org/pdf/1811.03119.pdf)
- [Approach that attempts to intergrate the uncertainty aspect directly into decision making](https://www.sergeysav.com/projects/rbmc/thesis.pdf)

Potentially Relevant
- [Deep Synoptic Monte Carlo Planning in Reconnaissance Blind Chess](https://proceedings.neurips.cc/paper/2021/file/215a71a12769b056c3c32e7299f1c5ed-Paper.pdf)
- [Supervised and Reinforcement Learning from Observations in Reconnaissance Blind Chess](https://arxiv.org/pdf/2208.02029.pdf)
- [Finding Optimal Strategies for Imperfect Information Games](https://cdn.aaai.org/AAAI/1998/AAAI98-071.pdf)
- [Regret Minimization for Games with Incomplete Information](https://proceedings.neurips.cc/paper/2007/file/08d98638c6fcd194a4b1e6992063e944-Paper.pdf)

Minimax Algorithm - Search that finds the best move for a chess player assuming the opponent plays optimally: https://www.youtube.com/watch?v=l-hh51ncgDI

