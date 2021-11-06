# SoccerPredict
Predict Premiere League soccer game scores using a Bayesian model

## Model

![image](https://user-images.githubusercontent.com/11340650/140603782-3b4a6f22-30e2-4c8c-8cda-c9825a35f24d.png)

## Example

November 6: Everton vs Spurs, predicted probabilities (Everton win 23.5%, draw 21.4%, Spurs win 55.1%), most likely score is 1:2, with estimated 11% probability.

```python
> game("Everton", # home team
        "Spurs",  # away team
        fit,      # fitted STAN model
        1000      # number of samples
        )
> {'away_win_prob': 0.551,
   'draw_prob': 0.214,
   'home_win_prob': 0.235,
   'most_likely_prob': 0.11,
   'most_likely_score': array([1, 2])}
```

## Parameters

![image](https://user-images.githubusercontent.com/11340650/140603916-43da3c1b-4ea0-4fa4-94e4-b5e0c3fe98bb.png)

Interesting findings:
- Best attacking: Man City, Man Utd, Liverpool, Leicester, Spurs, Leeds
- Best defending: Man City, Chelsea, Arsenal, Spurs, Liverpool
- Largest home-advantage in attacking: New Castle, Brighton and Wolves
- Largest home-advantage in defending: Southampton, Leeds, Sheffield Utd	and Spurs
