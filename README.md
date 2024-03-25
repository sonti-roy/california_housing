![Logo](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/th5xamgrr6se0x5ro4g6.png)


# Project Title
Machine learning model development for predicting median house value 


## Implementation Details

- Dataset: California Housing Dataset (view below for more details)
- Model evaluated: 
  - [Linear Regressor](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
  - [KNeighborsRegression](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsRegressor.html)
  - [SGDRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.SGDRegressor.html)
  - [BayesianRidge](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.BayesianRidge.html)
  - [DecisionTreeRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeRegressor.html)
  - [GradientBoostingRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingRegressor.html)
- Input: 8 features - Median Houshold income, House Area, ...
- Output: House Price

## Dataset Details

This dataset was obtained from the StatLib repository ([Link](https://www.dcc.fc.up.pt/~ltorgo/Regression/cal_housing.html))

This dataset was derived from the 1990 U.S. census, using one row per census block group. A block group is the smallest geographical unit for which the U.S. Census Bureau publishes sample data (a block group typically has a population of 600 to 3,000 people).

A household is a group of people residing within a home. Since the average number of rooms and bedrooms in this dataset are provided per household, these columns may take surprisingly large values for block groups with few households and many empty houses, such as vacation resorts.

It can be downloaded/loaded using the sklearn.datasets.fetch_california_housing function.

- [California Housing Dataset in Sklearn Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)
- 20640 samples
- 8 Input Features: 
    - MedInc median income in block group
    - HouseAge median house age in block group
    - AveRooms average number of rooms per household
    - AveBedrms average number of bedrooms per household
    - Population block group population
    - AveOccup average number of household members
    - Latitude block group latitude
    - Longitude block group longitude
- Target: Median house value for California districts, expressed in hundreds of thousands of dollars ($100,000)
## Exploratory data analysis

##### 1. Correlation between features were carried out to see if highly correlated features are there, so that redundancy could be removed from the features. 

![alt text](https://github.com/sonti-roy/california_housing/blob/main/plots/correlation.png)

##### 2. Correlation shows longitude and latitude are highly correlated and one could be removed from the features list.
![alt text](https://github.com/sonti-roy/california_housing/blob/main/plots/latitude_longitude_scatter_plot.png)

## Model fitting and evaluation

##### 1. Multiple models were evaluated for their performance and compared the R2 and MSE for the models.
![alt text](https://github.com/sonti-roy/california_housing/blob/main/plots/model_performance.png)

##### 2. The performance of GradientBoostingRegressor model was found to be the highest with very low MSEerror compared to other models that are evaluated.

| Model                     | R2        | MSE      |
|----------------------------|----------|----------|
| SVR                        | -0.020689| 1.017586 |
| LinearRegression           | 0.582674 | 0.416057 |
| KNeighborsRegression       | 0.136115 | 0.861259 |
| SGDRegressor               | 0.001655 | 0.995310 |
| BayesianRidge              | 0.582681 | 0.416051 |
| DecisionTreeRegressor      | 0.585701 | 0.413039 |
| GradientBoostingRegressor  | 0.772826 | 0.226484 |



## Cross valadation

To evaluate the GradientBoostingRegressor model further and check for over fitting, cross valadation is performed.


## Key Takeaways

What did you learn while building this project? What challenges did you face and how did you overcome them?


## How to Run

The code is built on Google Colab on an iPython Notebook. 

```bash
Simply download the repository, upload the notebook and dataset on colab, and hit play!
```


## Roadmap

What are the future modification you plan on making to this project?

- Try more models

- Wrapped Based Feature Selection


## Libraries 

**Language:** Python

**Packages:** Sklearn, Matplotlib, Pandas, Seaborn


## FAQ

#### How does the linear regression model work?

Answer 1

#### How do you train the model on a new dataset?

Answer 2

#### What is the California Housing Dataset?

Answer 2
## Acknowledgements

All the links, blogs, videos, papers you referred to/took inspiration from for building this project. 

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Contact

If you have any feedback/are interested in collaborating, please reach out to me at fake@fake.com


## License

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

