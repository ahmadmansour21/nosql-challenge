# nosql-challenge
The code for this challenge was written independently with the help of StackOverflow and Xpert AI tool

PART 1 - setup
The code can be found in NOSQL_setup_starter.ipynb in the nosql-challenge respository

The first step for this portion of the challenge was to enter the following line of code into terminal (as I am a MacbBook user): mongoimport --type json -d uk_food -c establishments --drop --jsonArray Resources/establishments.json --> this code allowed us to drop any pre-existing versions of the collection in order to start fresh in this database that we created called uk_food.

Next, we use the following code to create a connection to the database to make it possible to carry out our different queries: MongoClient(port=27017).

The remainder of this section is concerned with using different basic pymongo functions to query the database to return the result we desire. These include list_collection/database_names(), find_one(), update_one(), delete_many(), count_documents() and so on.


PART 2 - analysis
The code can be found in NOSQL_analysis_starter.ipynb in the nosql-challenge respository

This section is more analytical and therefore utilizes the same pymongo functions like find() and count_documents() to find particular information defined by a specific local authority name or hygiene rating. Then, these queries are used to create pandas dataframes displaying our results using pd.DataFrame.

Other methods are also employed such as {'$sort': {'count': +1 }} to sort the documents in descending order or print(results[0:10]) to print the first 10 results of the query. These more specific lines of code will depent on the particular goals.