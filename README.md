# **a Neural Network Analysis for Charitable Funding**
------------------------------------------------------

We used Tensorflow to design a neural network that uses binary clssification in order to determine if a charity which will potentially receiv funding from company **Alphabet Soup** will be successful or not.

## **Resources**
----------------
* **Data**: charity_data.csv
* **Software**: Jupyter Notebook version 6.3.0, Python Libraries: scikit-learn, Tensorflow, Pandas, and Plotly 

## **Overview**
----------------
Using Data acquired from *Alphabet Soup's* business team that shows which organizations received funding from the organization, we aimed to create a model to determine which organizations in the future would be successful if funded by Alphabet Soup. This dataset includes more than 34,00 organizations investment information, which includes a binary column that states whether invested money was effectively used. After cleaning the dataset and using sklearn's OneHotEncoder() to standardize the dataset, we're setting the outcome column as the target, with the remaining columns set as features to split the data into train and testing data. We then use sklearn's StandardScaler() and TensorFlow to determine accuracy using different nodes and activation functions.

## **Results**
----------------

### **Data Preprocessing**
--------------------------
* Our target was set to be the outcome column (**"IS_SUCCESSFUL**)
* We then removed the 'EIN" and "name" columns from the dataset, due to them being of little use in analyzing the dataset.
* The remaining columns were used as features in the analysis

## **Compiling, Training, and Evaluating Model**
------------------------------------------------

How many neurons, layers, and activation functions did you select for your neural network model, and why?
* Originally we used two layers that had 8 and 5 nodes. Our activation function for our input and hidden layers was relu, and sigmoid was selected for the output. 
![image](https://user-images.githubusercontent.com/93295751/159085154-40bb0707-ad63-4190-b7c7-2d97b67ba6ed.png)

*  First optimization attempt included three layers with 20, 18, and 11 nodes and a combination of relu and tanh activation functions:
![image](https://user-images.githubusercontent.com/93295751/159085204-6d23dca5-b823-46bd-a779-a3491d5e0497.png)

* Second optimization attempt included only two layers, using 9 and 6 nodes and the tanh function exclusively:
![image](https://user-images.githubusercontent.com/93295751/159085280-f575b5bd-748a-4bab-acad-7da71d448366.png)

* Third optimization attempt used three layers, including 7, 6, and 5 nodes, using a mix of relu and tanh:
![image](https://user-images.githubusercontent.com/93295751/159085371-039f528e-2d39-4ea4-9827-31b3447db1af.png)

* Fourth attempt used three layers with 25, 18 and 9 nodes each and relu activation:
![image](https://user-images.githubusercontent.com/93295751/159085429-c0c49003-1a06-4947-9846-4c2acc23c3fe.png)

## **Summary**
---------------

We were not able to successfully design a model to reach the target accuracy score of 75%. We tried increasing/ decreasing the number of buckets through different cut-off points on some of the feature's data. We tried using different activation functions but similarly were not able to achieve success. We could potentially increase the number of hidden layers in the model to achieve a higher accurracy score, however we then run the risk of overfitting our model to this dataset.




