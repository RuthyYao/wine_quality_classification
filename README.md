![front_image](./images/front_image.PNG)

# Wine Quality Classification Classification and Analysis

**Author**: [Ruthy Yao](mailto:zejia.yao@gmail.com)

## Overview

This project aims to help Riverwood Wine, which makes five to eight red wine products each year, to proactively manage the quality of their red wine products. Predicative analysis on the classification of wine quality between "high-quality" and "low-quality" wines shows that alcohol,sulphates,volatile acidity,density and total sulfur dioxide are the most important factors that contribute to a high-quality wine. The project specified a value range for each of the parameters. On top of that, Riverwood Wine can use this predictive model to adjust their sales and marketing efforts to improve the resources allocation. 

## Business Problem

Riverwood Wine is a renowed winemaker in the industry. Every year, they participate in the industry rating and award. Wining the award will greatly enhance their brand value and boost their sales. Historically, at least three of their products would get the "Spectatular Wine" award. However, in recent years, their wins became very unpredictable - in some years, none of their wines got an award. 

The leadership team would like to have a better understand from the physiochemical properties perspective, what makes a 'great" wine. With those insights, Riverwood Wine can proactively manage the fermentation process - better control over the quality of their product and increase the chances of winning the industry award. Furthermore, they would like to self assess their products so they can allocate their sales and marketing budget to the best products.


## Data and Methods

The dataset comes from the red variants of the Portuguese "Vinho Verde" wine (see [Cortez et al., 2009], http://www3.dsi.uminho.pt/pcortez/wine/), which contains 1599 entries of red wine products. Te data features 11 physiochemical properties and the wine quality in ordinal numbers from 1 to 8. 

This project employs the descriptive and predictive analysis to identify the most contributing factors for a high-quality wine. Based on the 11 physiochemical parameters, it can predict whether a wine will achieve the "high-quality" status. This provides great insights on what makes a "high-quality" wine, the most determining physiochemical properties and the desirable range for each.  

Three machine learning models are trained and assessed based on the accuracy score and the F1 score (a combination of precision and recall). The Random Forest model triumphed over the other two algorithms - Logistic Regression and Decision Tree. The "feature importance" technique was employed to select the parameters that contributed the most to the "high-quality" status. For the top five most important factors, we use a quartile distribution analysis to decide the value range for each parameter. 

## Results and Insights

The final model using Random Forest algorithms achieve a prediction accuracy of 93.4% and a F1 score (a combination of precision and recall) of 71.2%.

The ranking of the 11 parameters based on the level of contribution to the quality classification is as following.

![Feature_Importance](./images/feature_importance_random.png)

For the top five parameters, the desirable value range based on where the most data lies are: 

* Alcohol - to control between 10.8 and 12.2;
* Sulphates - to control between 0.65 and 0.86;
* Volatile acidity - to control between 0.3 and 0.49;
* Density - to control between 0.9947 and 0.9974;
* Total sulfur dioxide - to control between 17 and 43.

### Nest Steps

Further analyses could yield additional insights to further improve the prediction at Riverwood Wine.
    
- **Enlarge the sample size** - This dataset has only 1599 entires of the wine product with only ~230 classified as "high-quality". Enlarge the sample size will improve the predicative accuracy.

- **Analyse the interacted features** - Some physicochemical properties are interdependent. Build interaction features will improve the predicative power. 

- **Introduce the white wine dataset** - - This model can be applied to dataset of white wine products. Compare and contrast the results from the two different prodducts' dataset will yield additional insights around the common factors vs the product-specfic factors so Riverwood can target the fermentation techniques to improve.  

## For More Information

See the full analysis in the [Jupyter Notebook](./wine_quality_analysis.ipynb) or review this [presentation](./wine_quality_analysis_presentation.pdf).

For additional info, contact Ruthy Yao at [zejia.yao@gmail.com](mailto:zejia.yao@gmail.com)

## Repository Structure

```
├── Data
│   └── winequality-red.csv
├── images
├── wine_quality_analysis.ipynb 
├── wine_quality_analysis_presentation.pdf
└── README.md
```
# House_valuation_tool
