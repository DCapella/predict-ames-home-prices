# Ames Iowa Data
We will be looking at 2 different CSV files of features from housing reports in a csv file. This data is collected from Ames, Iowa and was got from Kaggle.
* [Training Data](./datasets/p2_data/train.csv)
* [Testing Data](./datasets/p2_data/test.csv)

## Statement
Which features affect sale price the most? And which features do not affect it at all?
    
## Data 

All of the major points for the data and description can be found out here.

### Points of Interest

#### Cleaning Data
* When cleaning the data, I first tried to change descriptions into rating numbers but that seemed to have a negative impact on my model so I quicly switched to dummy columns that definitely improved it.
* On the null values, I used different columns to find the mean for similar houses. I believed this to be better than setting it to 0 or getting rid of the column.        
* There are some outliers in gorund livin area that I will not fix because I believe it will be dependent on the neighborhood which I will pull into account as well.

#### Models
* Linear regression and LassoCV models had very similar residuals which made me look into the distribution of true y.
* Decided to use power transform with LassoCV and it turned out a lot better, still changes to be made.
* After looking at the coefficents and getting rid of some unncessary features; the model worked even better.

## In Conclusion
* It seems there are a lot of different features that will affect the sale price of a house in Ames, Iowa. However, lot frontage had no impact.
* Above Ground Living Area seemed to have the most impact with only 29¢ per square foot.
* Overall Quality had an impact of 21¢ per rating number.
* Year Built had an impact of 14¢.
* Runner up Overall Condition with an impact of 11¢ per rating number.

 
    