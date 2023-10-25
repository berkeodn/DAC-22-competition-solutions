# Data & Analytics Challenge'22 Solutions
This competition consists of two stages, each lasting one week:

1- Armut Project

Armut is an online marketplace that meets customers with local service providers. When a customer creates a job request, ML-based matching algorithms are triggered and determine possible service providers. Finally, job opportunities are sent to those providers. If a provider wants to quote such a job opportunity, then the platform makes them meet. In this project, we provide you with the job opportunity dataset and ask you to predict which opportunities were quoted and which were not.

## Dataset Description
### File Descriptions
TRAIN.csv: - there is a train data. ISQUOTED in this file is our target variable.
TEST.csv - the test set
sample_submission.csv - a sample submission file in the correct format
JOBDETAILS.csv - supplemental information about the data
JOBQUESTIONS.csv - supplemental information about the data
ProLoc.csv - supplemental information about the data

### Data Fields
### Train-Test Set
OPP_CREATEDATE: Opportunity Create Date for Provider
JOBID: Unique identifier for jobs
PROID: Unique identifier for providers
ISQUOTED: Provider was quoted such opportunity or not. It is our Target Variable

### Job Details
JOB_CREATEDATE: Create Date for each job. Jobs are created by customers.
JOBID: Unique identifier for jobs
SERVICEID: Unique identifier for Serviceid. Jobs are categorized under services like Cleaning, Moving, Private Lesson etc.
OUTER_LOC: Outer (Main) Location of the job. (like “Beşiktaş”)
INNER_LOC: Inner (Sub) Location of the job. (like “Bebek Mh.”)
JOB_PRICE: Average Price of each job

### JobQuestions
JOBID: Unique identifier for jobs
QUESTIONID: Unique identifier for job specific questions. Like “Hangi konuda özel ders almak istiyorsunuz?”
ANSWERID: Unique identifier for job specific answers. Like “Matematik | Fizik”
ProLocations
PROID: Unique identifier for providers
OUTER_LOC: Outer (Main) Location of the Provider. (like “Beşiktaş”)
INNER_LOC: Inner (Sub) Location of the Provider. (like “Bebek Mh.”)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

2- Invent Analytics Project

Seasonal demand planning is very crucial for retailers as it gives them a strategic plan on how they will meet the demand throughout the whole season. The constantly transitioning circumstances, on and off promotions, changing gustos, newly launching products, or new additions to the store chain are what makes it a little bit complex problem. Despite the complexities that the problem has, the ultimate gains are preventing stock-outs that cause loss of money and holding excess stock causing storage costs and product expirations, thanks to seasonal demand forecasting executed well in advance. BUYAK challenges its competitors to build a model that yields the most accurate product forecasts for the seasons.

## Dataset Description
### Data
The competitors will be asked to predict the total product demand for each week in the season. The training data shows the sales quantity for each product and week and some additional informative metrics. There are also 2 additional file that show the product attributes and holidays that may shift the demand.

### File Descriptions and Data Field Information
Train.csv
-Shows the target column sales_amount by date (representing weeks) and product_id. There is a unique id column corresponding to each row.
-The price column shows for how much the product was selling in total that week whereas the discount column shows the discount percentage that was applied for the product that week.
-The on-promotion column shows whether the specified product was on promotion that week or not. (1 for on promotion, 0 otherwise) In addition, promotion type shows the promotion description and type.
-The sThe season type column shows which season the specific product belongs to.
-The store count column shows how many stores this product was trading in.

Test.csv
-Test data shows the date and product_id and season type to be predicted along with store count, on promotion and promotion type.
-The id column in the test data matches the id column in the submission file.

Sample_submission.csv
-Submission file where the predicted numbers to be provided for each id in.

Product.csv
-The id column shows the corresponding product_id’ along with the other attributes of the products.
-Category_1, category_2 and category_3 represent the hierarchy levels.
-All the other columns show an attribute for colour, style or cotton type etc.
-Please note that there are some products with missing values for some of the columns.

Holidays.csv
-The file shows the days and the holiday descriptions that can be utilized building the model.

Submission File
-For each id in the test file, the competitors should predict the demand quantity. The expected file should look as below with a header in it.
