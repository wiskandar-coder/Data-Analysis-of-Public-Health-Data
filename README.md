# Data-Analysis-of-Public-Health-Data
The project is an idea for food-related application using Open Food Facts data.


The idea is a product recommendation based on nutrition score of the food.

  I- User input the product name or scan the barcode of the product.\
    II- Application search for the product in the database and the nutritional information related to the product.\
        If the product is not in the database, the application output to the user that the product in not found in the database.
        If the product is in the database, the application proceed to the next step.
            III- Application check of the product:
                If the nutrition grade of the product is a, the application will not recommand another product to the user, the application will just display the nutrition grade of the product to the user.
                If the nutrition grade of the product is not a, the application search for similar products in the database based on the categorie of the product. Then the application will proceed to the next step.
                    IV- Application selection of better nutrition grade products: From that pool of similar products, the application select only those with better nutrition grade.
                        V- Application selection of the best nutrition score product: From those products with better nutrition grade, the application will display to the user the product with the best nutrition score.


The project is divided into two sections:
- First is the cleaning of the data.
  I started by importing the data from Open Food Facts website https://world.openfoodfacts.org/ and the definition of the variables can be found in https://world.openfoodfacts.org/data/data-fields.txt
  Then, I cleaned the data by removing the features with more than 80% missing values, 
  
- Second we analyse the features selected.
