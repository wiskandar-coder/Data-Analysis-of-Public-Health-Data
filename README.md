# Data-Analysis-of-Public-Health-Data
The project is an idea for food-related application using Open Food Facts data.

The idea is a product recommendation based on nutrition score of the food.

![image](https://user-images.githubusercontent.com/64427335/233734187-ef41d2b2-0fce-4399-bde3-8ab7a6d33674.png)

~~~
I- User input the product name or scan the barcode of the product.
II- Application search for the product in the database and the nutritional information related to the product.
    - If the product is not in the database, the application output to the user that the product in not found in the database.
    - If the product is in the database, the application proceed to the next step.
III- Application check of the product:
    - If the nutrition grade of the product is a, the application will not recommand another product to the user.
    The application will just display the nutrition grade of the product to the user.
    - If the nutrition grade of the product is not a, the application search for similar products based on the product categorie.
    Then the application will proceed to the next step.
IV- Application selection of better nutrition grade products:
    From that pool of similar products, the application select only those with better nutrition grade.
V- Application selection of the best nutrition score product:
    From those products with better nutrition grade, the application display to the user the product with the best nutrition score.
~~~

The project is divided into four sections:
~~~
1- First is the cleaning of the data.
    I started by importing the data from Open Food Facts website https://world.openfoodfacts.org/.
    The definition of the variables can be found in https://world.openfoodfacts.org/data/data-fields.txt
    Then, I cleaned the data by:
    - removing features with more than 80% missing values
    - removing food products with missing values on the nutritional informations
    - removing food products with wrong nutritional informations
    - removing food products without name or wrong barcode
    - removing duplicates on the product name and brand
2- Second we treat the missing values using:
    - iterative imputer for the highly correlated features
    - the median of the feature according to the category of the product
    - RandomForestClassifier for the other categorical columns like nutrition score and grade
3- Third we analyse the selected features:
    - univariate analysis of each feature
    - bivariate analysis to check for correlation between the features:
        - correlation factor using pearson method between the numerical features
        - ANOVA analysis between the categorical features and numerical features
            (because of asymetrique distribution of the numerical features,
             I should use Kruskal-Wallis test instead of ANOVA)
    - multivariate analysis using dimension reduction of PCA
4- Finally, arguments about the feasability of the idea are given
    (what missing in this project is the actual application)
~~~

The first and second points are covered in the notebook 'Cleaning_notebook'.\
The third and fourth points are covered in the notebook 'Analysis_notebook'.\
Finally a powerpoint presentation of the project is also included.
