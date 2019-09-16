### Bixi use and gas prices: negative result

We tried to model how much Bixi use would change when gas prices changed, but the model was too unstable with the data we had.

The main file is `kaggle/bixi/training.ipynb`.

#### Tool used

XGBoost.

#### Data sets

We spent a lot of time trying to get data sets, and eventually got:

- Gas price data set
- Bixi dataset
- Weather
- Cars waiting at intersections

The last data set turned out not to be useful for this purpose, because the intersection changed arbitrarily every day, so a fine-grained time-series comparison was not really possible. However, we used the first three to look for dependence of Bixi use on gas price, controlled by weather and time.

#### Explanation

We tried to analyse 2016-2017, which was available in both the Bixi dataset
and the gas price data set, but unfortunately there were no large gas price changes in that time.
The model was able to predict the Bixi use fairly well from time of day, weekday, temperature, and weather description (sunny, cloudy...), but it did not see much dependence on gas price.
