# MarketBasketAnalysis
Mini Project

**Implementation:**


Firstly we need to import different packages like collections, NumPy, pandas, and mlxtend for all the necessary operations in this project. If you are using google colab you need to mount your drive to the colab and ensure that the data is saved in drive.
Now we read the data from the dataset, analyse the data and perform the following operations:

**Data Cleaning:** 
It basically means that we need to remove all the unnecessary values like duplicates, incorrect, non proper format values and incomplete data, etc. 
The data is not following proper format, so we make a more meaningful data out of our dataset.
In this data there will be all a lot of null values because each customers cannot order every single item on the menu. We fill out all the null values with 0

**EDA(Exploratory data Analysis):** 
In this phase we generally represent the data in the form of graphs and statistics to perceive the data to discover patterns the data is following.
In this we have taken the top list values of each combolist using bar graph.

**Data-prepocessing:**
A technique used in data mining which is used to process any data into meaningful one and in the proper format.
We used a function called encode_units which primary function is to fill the values with 0 and 1 for our data to acquire the properly formatted data for further usage.

Now we require all the support values of the items in the dataset. For that we dump all the item values in the apriori method which we imported from mlxtend package. We also give the minimum support required support values. Now the support of all the possible combinations of items in data is returned.

Now support value data which is returned is given to association_rules method in mlxtend package. We get the all the associations of the items now with values like support of (antecedents, consequent, both antecedent and consequent), confidence, lift, leverage and conviction of the respective associated items.

**Model Building:**
We take lift as our priority value in our Model and drop all the rest values in the data. Now we use Ordereddict from collections package and store all the values in the data into the ordereddict and this values into a list called combos_list

**Final Result:**
Finally we filter out all the combos based on the length of the items present in the combos_list and store it in combos2(2 items), combos3(3 items), combo4(>=4 items).
We write a function all the respective combos so that the dataframe of the respective combos with the top 5 lift values from each combolist is returned
