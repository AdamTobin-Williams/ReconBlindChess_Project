# ReconBlindChess_Project
This is a submission into the Reconnaissance Blind Chess competition held by the Johns Hopkins Applied Physics Laboratory from the participants Jeremiah Fan, Amaiyah Johnson, Adam Tobin-Williams, and Nico Valle

Competition: https://rbc.jhuapl.edu/challenge

Library: https://reconchess.readthedocs.io/en/latest/

Slides: https://circuitinstitute.slack.com/files/U010M1CAJ0M/F05G76Z8AJD/bytes_challenge_chess_2023.docx?origin_team=T89L0S73J&origin_channel=C05GPT9DNF4

Notes:
## Recon Blind Chess Notes
Piece Tracking
  The computer tracks all possible locations of opponent pieces and displays them in a semi-transparent overlay. This overrides the display mode as longs as tracking is active. If the number of possible boards exceeds 5,000 at the end of your turn, the assistant turns off.
  Bot should be able to do this (or something similar)
Things the Bot will have to Consider
  The most logical moves the opponent could have made (if the bot failed to sense what move was made)
  Where the opponent’s piece moved FROM as well as moved to
  Where the opponent most likely sensed
  What would the most logical move be in regular chess?
Other Ideas
  Is there a way to calculate the bot’s Elo? Would this be helpful at all?

## Basic chess bot Ideas:
Game state evaluation: quantifying the value of a specific position and trying to take moves that improve that value
  Assign values to specific pieces and positions, tweaking these values could improve bot
  Value of sensing positions based on your position and guess of the opponents'? Aim for sensing in such a way that it collapses possibilities to enable piece tracking?
Search tree: Looking moves ahead to find the best outcome and retracing the steps to get there
  Search tree for sensing patterns? Chaining together 3x3 searches to set up for attacks?

Search Algorithm Video: https://www.youtube.com/watch?v=l-hh51ncgDI

Possible solution?: https://github.com/ginop/reconchess-strangefish
