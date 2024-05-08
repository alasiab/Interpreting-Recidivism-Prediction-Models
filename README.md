# Interpreting-Recidivism-Prediction-Models
# Who Painted This? Van Gogh, Dali, or Picasso?

Final Project for Interpretable Machine Learning Spring 2024

Link Google Colab Notebooks: 
LIME on General Model: https://colab.research.google.com/drive/1KCBTrKf2lJASUXW3Hd5IeNJa_2-Udm1J?usp=sharing
Female Only Data LIME: https://colab.research.google.com/drive/1kRR39Xpd0VA1el8BADaZNSsnb3mXPoAM?usp=sharing
Male Only Data LIME: https://colab.research.google.com/drive/1QS27xPML7nD7W9xc6VdKmydQwO_QXq1N?usp=sharing
Gang Affiliated Only Data LIME: https://colab.research.google.com/drive/11nDol4SLAU8FY_jyzJtf4XwMiKawNzSO?usp=sharing
Not Gang Affiliated Only Data LIME: https://colab.research.google.com/drive/1Qy9MvRNzsbdx5uPcXLQ_JF9tVeoUqpgp?usp=sharing
Accurate vs Inaccurate Prediction LIME Summaries: https://colab.research.google.com/drive/1mxy2TsRqwmuJcZi1ai3M8K0Yt_kecJzC?usp=sharing

## Introduction 
n America’s prison and jail population is over 2 million and rising. There are many
approaches to try and solve the mass incarceration problem in America, many of which involve
the concept of recidivism. Recidivism refers to the likelihood of a defendant to re-offend after
release. Models to predict recidivism are currently in use across the country by judges, parole
boards, and other agencies, sometimes as a part of the decisions regarding a defendant’s
sentencing. In the case of black box models, the lack of transparency is upsetting and leaves the
model at risk for unintentional bias. To make the use of these models equitable for all, it is
imperative that the public have an understanding of how they work.

## Methods 
This project analyzed a neural network trained on a dataset containing 54 data fields
on 26,000 defendants from the state of Georgia. The dataset had a baseline accuracy of 57.7%
and the model(s) achieved accuracy ranging from 70% to 74%. While this is not the highest
accuracy, it is still higher than the accuracy of some models in use today. The low accuracy may
affect the interpretability, however.

## Results 
The main model was analyzed using the LIME library. The top features contributing to
the predictions were consistently percent days employed, gender, age at release, and gang
affiliation. To try to further explain the model, it was trained on datasets split on top features.
The model was trained on only male and only female data. The explanations for only male data
lined up with the general model, but there was more nuance in the only female data model
explanations. The possibility of different features contributing to accurate vs inaccurate
prediction instances was also explored, though nothing significant was noted.

## Discussion
It is difficult to determine if the model is equitable based on just this analysis alone.
Further exploration on the characteristics of the subsets of accurate vs inaccurate predictions,
further splitting the data and training models for more in depth explanations, and determining if
other features may be represented by proxy in the features in the explanations would all be
helpful for further consideration.

