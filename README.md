# Marketing-mix-modeling
How efficient is this marketing strategy?

## Situation
Our client promotes its product on different channels (e.g., TV, radio, online, etc.). 
We had data about his marketing strategy, and we had to analyze it. Is it going well? Is there something that can be improved?

To answer these questions, we collected sales history over two years, the history of the client's marketing investments, and other indicators (e.g., GDP, amount of tourists, etc.) we suspected might influence the client's business.

## Action

First of all, we **did an overview** of the data. What does it look like? What's going on in the client's business? 
We noticed that sales are growing and that marketing activities are intermittent. Nothing interesting.

Secondly, we **joined two datasets** (about marketing activities and economic indicators).
The first one is a weekly dataset, and the second is monthly. So we **interpolated one dataset** to convert it from monthly to weekly.

Thirdly, we needed to **select** the most **essential features** from the dataset. For this, we used a correlation matrix. 
We removed features that don't correlate with sales and features that strongly correlate with each other.

Fourthly, we **transformed data** about marketing investments because advertisement has a **delay effect** and **diminishing returns**. Therefore we want to incorporate it into our model.

Fifthly, we used **linear regression** to predict sales using economic factors and marketing activities.

So, in the end, we had linear coefficients for every channel (e.g., TV, radio, online) and knew the contribution for every channel. 
Based on this, we can decide what works and what doesn't. And we can find the **best marketing mix** (it's the constrained optimization problem).
