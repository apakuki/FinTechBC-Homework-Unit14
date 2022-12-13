# Machine Learning Trading Bot

![Decorative image.](Images/14-challenge-image.png)

Now, it's time to take what you've learned about machine learning and apply it to new situations. For this optional assignment, you'll create an algorithmic trading bot that learns and adapts to new data and evolving markets. Be sure to give it your all -- as the skills you hone will become powerful tools in your FinTech tool belt.

## Background

In this Challenge, you’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. Your firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, your firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave your firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. You’re thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, you’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

## What You're Creating

You’ll combine your new algorithmic trading skills with your existing skills in financial Python programming and machine learning to create an algorithmic trading bot that learns and adapts to new data and evolving markets.

In a Jupyter notebook, you’ll do the following:

* Implement an algorithmic trading strategy that uses machine learning to automate the trade decisions.

* Adjust the input parameters to optimize the trading algorithm.

* Train a new machine learning model and compare its performance to that of a baseline model.

As part of your GitHub repository’s `README.md` file, you will also create a report that compares the performance of the machine learning models based on the trading predictions that each makes and the resulting cumulative strategy returns.

## EVALUATION REPORT

* Establish a Baseline Performance

The data for this exercise was imported without any issues. I was then able to generate trading signals using short- and long-window SMA values of 20 and 100 respectively. Next, I split the data into training and testing datasets, with a training dataset size of the first 3 months of the complete datatset. The `SVC` classifier model was then used to fit the training data and make predictions based on the testing data. Following that I created a predictions DataFrame that contained columns for “Predicted” values, “Actual Returns”, and “Strategy Returns”. This was used to generate a cumulative return plot that showed the actual returns vs. the strategy returns. A copy of this plot can be found here:

[Baseline](Starter_Code/Resources/Baseline.png)

* Tune the Baseline Trading Algorithm

I chose to tune the Baseline by increasing the training window size to 6 months and 12 months, and also by reducing the long window size to 20. The best result was obtained when the training window was at 6 months and the long window size remained unchanged at 100 days. The comparison of results can be seen in the following plots: 

[Baseline 20 day long window](Starter_Code/Resources/Baseline_long_window20.png)

[Baseline training end 6 months](Starter_Code/Resources/Baseline_training_end_6months.png)

[Baseline training end 12 months](Starter_Code/Resources/Baseline_training_end_12months.png)


* Evaluate a New Machine Learning Classifier

I chose two Machine Learning Classifiers to compare results, the first being Logistic Regression and the second being AdaBoost Classifier. Although AdaBoost improved accuracy from 53% to 86%, neither was able to outperform the results from extending the training window to 6 months. This of course based on the dataset given.

The comparison of the two Machine Learning Classifiers can be seen here:

[Logistic Regression](Starter_Code/Resources/Baseline_against_LR.png)

[AdaBoost](Starter_Code/Resources/Baseline_against_AdaBoost.png)


---

© 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
