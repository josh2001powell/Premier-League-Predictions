# Premier-League-Predictions
Predicting premier league matches using different machine learning techniques

Current plans:

Try different machine leanring algortithms

1) Linear regression - This model should be useful for converting stats involving shots into goals due to the linear relationship between twice as many shots should mean twice as many goals on average. Could include keeper strength into these metrics or a general team's likliehood to shoot from low xg positions. I could also try to create models for each team but I worry the lack of data for individual teams would hinder the very nature of machine learning benefiting from huge anmounts of data; including more data would mean going back several seasons which no longer captures the team's current ability which can flucatuate massively.

2) Random Forest - I expect the Forest model to be able to handle less obvious/direct stats on xg and I would hope that with enough simulation it might be able to capture mroe complex relationships such as possession stats/xga/opponent strengths. It's hard for a linear model to classify these and will probably find very low coefficients.

3) Poisson Model - Similar to LR but this may be particulary suited to predicting goals. This is because predicted goals can only be positive and should be rounded to an integer value anyway if trying to predcict the actual result rather than some arbitrary 1.765... goals. Both of these are inherent traits of Poisson statistics and the discretisation from the model lines up well with goals being integer values.

4) Neural Network - This should be the best for understanding any non-linear metrics, this could be advantageous for a large amount of prediction metrics as I can only really see a linear relationship occurring for shooting metrics. However, typically neural networks need vast amounts of data which might require many seasons of data and potenitally including multiple leagues to reach a large enough quantitave base. In theory this should work fine if all the teams behave in similar ways when considering metrics but for teams with extreme tactics (where the game changes massively when said team is winning or losing) it might struggle to create useful relationships. Naturally, we will also need to consider the loss function and try to avoid becoming stuck in local minima.

5) Clustering - Some type of clustering could help classifying the playstyle of teams which I noted could be a problem for other techniques. Grouping very attacking teams such as Man City with Chelsea and Liverpool together and then grouping more defensive "low block" teams such as Arsenal and N'Forrest could work. This may not work as it own technique but I could try to  implement this playstyle classificaition into a metric; low block teams would lower the xg of the opponent whilst generally attacking teams have a naturally higher likliehood of scoring but also coneceding.
