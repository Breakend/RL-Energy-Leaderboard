# RL-Energy-Leaderboard

## Check out the site!

https://breakend.github.io/RL-Energy-Leaderboard/reinforcement_learning_energy_leaderboard/index.html

## Contributing 

If you have data you'd like to share, please send a pull request with your log files from the <a href="github.com/Breakend/experiment-impact-tracker">experiment-impact-tracker</a> in the format you see in the data/ folder.

Specifically, we'd like to see **at least** 5 random seeds per experiment with the impact tracker logs. Additionally, we expects an eval_test.csv in the same directory as contains the impacttracker folder. This file should be in the same format as the others you see here. The first line contains hyperparameter settings. The second contains the headers. All lines after that are standardized evaluations of 25 episode rollouts on separate envs every 250k learning steps until 5M timesteps are completed. To see how evaluation rollouts can be done, see: TODO.

Add a line to the leaderboard_generation_format.json file with a regex on how to find your results (and any description/pointers to code you might have) and then submit a pull request! We'll recompile the site once it's accepted and your results should show up.

## Generating the Leaderboard Website

This was auto-generated with the experiment-impact-tracker appendix generation script:

```bash
create-compute-appendix ./data/ --site_spec leaderboard_generation_format.json --output_dir ./docs/
```
