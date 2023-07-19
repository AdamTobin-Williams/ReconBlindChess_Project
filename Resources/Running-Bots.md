Setting up environment with conda (For Mac OS)

1. After downloading the repository, open the terminal
2. Create a conda environment from the repository's YAML file by pasting file path ```conda env create --file PATHTOYAML``` (ex. .../ReconBlindChess_Project/environment.yml)
3. Activate conda environment ```conda activate reconChess```

Playing against stocky-interface 
1. Create a environment variable named STOCKFISH_EXECUTABLE, stockfish is included in this repository ```export STOCKFISH_EXECUTABLE=/absolute/path/to/stockfish```
2. Set up match against the bot ```rc-play /path/to/bot```
