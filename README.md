# customer-churn-analysis

Analysis of the customer churn dataset on Kaggle at: https://www.kaggle.com/datasets/undersc0re/predict-the-churn-risk-rate.

This analysis was done using Python 3.13.5. Package management was done using `uv`. If using `uv`, the environments can be setup using:

```bash
uv sync
```

If you are using pip, use:

```bash
pip install requirements.txt
```

The data was stored in the same level as the notebooks under a `data` folder with the filename as `churn.csv`.

# Summary of Analysis

This analysis has been provided in the conclusions of the notebooks but is reproduced here as well.

## Recommendations to the business

From the analysis, it is clear that engagement metrics are not driving the churn but it is the value provided to the users. To address churn, the value provided to users would need to be addressed and strategies would need to be developed around this. 

`avg_transaction_value` and `points_in_wallet` show a separation between churners and non-churners. This separation is more than what can be seen in engagement metrics such as time spent or frequency of login. Non-churners tend to have higher `points_in_wallet`, and their `avg_transaction_value` also seems to be high. From a modelling perspective, it is also apparent that engagement metrics are not a key driver of risk classification for customers. 

Putting together the analysis of the categorical and continuous features, it seems that churn may be happening due to the value that the users are able to derive from the service, rather than to do with engagement (like a social media app). This is because engagement metrics such as time spent or frequency of login do not seem to be strong signals for churn.

Additionally, the lower tiers membership categories have a higher churn rate as well, and to retain these customers, strategies need to be developed that target this user group specifically. 

It is recommended that the results of this and the future modelling results be used to determine which users to reach out to keep these users engaged and fulfilled with the services of this app.

### Future Analysis

To address the limitation of negative feedback likely being correlated with the `churn_risk_score`, next iterations of the analysis would need to focus on considering modelling churn without the feedback or consider alternate feature engineering strategies.
