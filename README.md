
<h2 style="text-align: center;">Analysis and Price Prediction of Londrinas Real Estate</h2>

`Analysis and Price Prediction of Londrinas Real Estate` is a project that depicts data analysis regarding real estate in the city of Londrina in Paraná, Brazil, and trains a regression model to try and predict the price of a real estate. The data is collected from real estate sites and are anonymized to avoid any privacy issues. 


The goal of this project is to practice concepts of data analysis and data science using real world data. The usage of real world data makes this work relevant, as it reflects characteristics and complexities that can be used to find insights that can be applied to the real world.  

The tools used in this project are:

- Python
- Pandas, Matplotlib, Seaborn
- Scikit-Learn
- SHAP
- Folium, GeoJSON  


The project is divided as following: 

### 1. Dataset and Data Analysis
The dataset consists of about 25.000 real estates containing the features: **`Neighbourhood`**, **`Square Meters`**, **`Number of Rooms`**, **`Number of Bathrooms`**, **`Garage spots`** and **`Price`** in brazilian **`Reais`**(**R$**). In the **data analysis** notebook, i perform transformations on the data to get it ready to the model notebook and further analysis, which includes the most expensive and least expensive neighbourhoods to have a real estate, based on the mean of the price of each neighbourhood real estates square meters. After that, i prepare data to make an interactive map using **folium**. 

### 2. Interactive Choropletic Map
The interactive choropletic map was generated using a **`.shp`** file made available by Londrina's prefecture in their website, which was then converted to a **GeoJSON** file and using **Python's** **`Folium`** to generate the final interactive **choropletic map** which is split into all of the city neighbourhoods that displays the name of the neighbourhood and its mean price of square meters when hoved over and also display a range of colors in proportion to the prices of the square meters of each neighbourhood. Despite not showing all of the neighbourhoods cointained in the dataset, this map produced a good result and represents well the mean prices of each neighbourhood. Link for the interactive choropletic map : [Interactive Map](https://zaniandrei.github.io/Real-Estate-Price-Prediction-in-Londrina/mapaLondrina.html)


### 3. Prediction Model
The prediction model notebook contains tests for 2 different models, in order to decide which one is the best to perform this task. The two models in question are: a regression model (**`Ridge Regression`**) and an ensemble model (**`Random Forest`**). The tests made for **Ridge Regression** found an **R² score** of about **`0.74`** and a **Mean Absolute Error** of **`309282`** with the model taking about 1 and a half second to train and the tests for the **Random Forest** scored a **R²** of about **`0.88`** and a **Mean Absolute Error** of **`156361`** with the model taking about a minute to train. It is concluded then that the **Random Forest** model can perform better than the **Ridge Regression** model, but it takes much more time to train, because ensemble models are more complex than regression models.     



<h2 style="text-align: center;">Results Discussion and Next Steps</h2>

This project achieved good results in general, but there is room for improvement. Like the choropletic map, which lacks data of most real estate in the dataset, and the machine learning model, which can be improved greatly with the adding of more features in the data or different models. So, for future works, i would like to find a way to fit all of the real estate in Londrina into the publicly available neighbourhoods map using Google Maps and also to find new features for the data, like if the real estate is a house or apartment or if it is furnished or not, and also test more artificial inteligence models, like Neural Networks models or other ensemble models that makes usage of regression.    