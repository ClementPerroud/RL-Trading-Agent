# Profitable Trading Agent working with Reinforcement Learning

Creating my own Reinforcement Learning TradingAgent. I suceeded at making a profitable bot (with fees ~ 0.1% = Binance Trading Fees)

## How to use ?
My projet needs both of my personal projets to work.
* The first my Gym Trading Environment (the simulation in which the agent will be trained)
* The second is my Rainbow Agent (a improved version of Deep Q Network aka. the AI)

## Steps
Run `manage_file.ipynb` cells to download datasets and process them. (BTC/USDT and ETH/USDT from 3 exchanges)
Then, run `training.ipynb` cells to train the agent in the environment with to preprocessed datasets.

## Project description

Validation data are fully seperated from training data (by date) to guarantee safe results.
One validation is made every 30 000 steps on 5 parallelized training environment. Then the agent is evaluated on 5 validation environment.

## Validation Results

After 1h of training :
```bash
Market Return : -36.93%   |   Portfolio Return : -4.01%   |   Position Changes : 12.43%   |   Max Drawdown : -37.56%
Market Return : -36.93%   |   Portfolio Return : -19.18%   |   Position Changes : 12.51%   |   Max Drawdown : -49.14%
Market Return : -24.95%   |   Portfolio Return : -14.29%   |   Position Changes : 11.30%   |   Max Drawdown : -29.71%
Market Return : -36.78%   |   Portfolio Return :  7.91%   |   Position Changes : 11.34%   |   Max Drawdown : -29.87%
Market Return : -24.96%   |   Portfolio Return : -3.79%   |   Position Changes : 11.69%   |   Max Drawdown : -30.22%
```

After 2h of training :
```python
Market Return : -36.99%   |   Portfolio Return : 114.42%   |   Position Changes :  8.90%   |   Max Drawdown : -31.45%
Market Return : -36.96%   |   Portfolio Return : 91.60%   |   Position Changes :  9.24%   |   Max Drawdown : -42.20%
Market Return : -36.96%   |   Portfolio Return : 98.06%   |   Position Changes :  9.25%   |   Max Drawdown : -42.20%
Market Return : -36.93%   |   Portfolio Return : 78.73%   |   Position Changes :  9.58%   |   Max Drawdown : -35.20%
Market Return : -36.94%   |   Portfolio Return : 127.78%   |   Position Changes :  9.30%   |   Max Drawdown : -37.20%
```

Then, the agent begin to overfit.
