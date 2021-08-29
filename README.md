
Follow the instructions from the website below to install Spark and use Pyspark from Jupyter in Window

https://bigdata-madesimple.com/guide-to-install-spark-and-use-pyspark-from-jupyter-in-windows/

Copy this folder in the path

Browse using relative path of the file in jupiter notebook and open the CodingChallenge.ipynb

Run the the script by using shift + Enter key

TEST RESULTS

The python code has been saved as notebook which shows the output of the the execution

Assumptions/Tradeoffs
---------------------

1. Hashkey is created based on the combination of AccountId and Fibre columns to uniquely identify the records
2. String column $ Amount is coverted to "float" for calculation purpose
3. Timestamp from Implemented Date and Request Date are removed. It is then converted as "Date" format to perform operation on date
4. Filter questionable data
	a. Assuming that Account Id should be only integer and removing decimal number records 
	b. Assuming that the Fibre column should contain only [A-z] , [a-z],[0-9]_ and removing records which contain "+"
5. The data frame is then converted into multiple json files with each file containing 1000 records
6. Json serializer doesnt allow data type "date" hence it needs to be converted into a string
7. DateTimeEncoder class has been created to convert it as string
8. Class Fast_response gives the required output based on the Post Codes 
9. Class Fast_response provides the list of Top Agents based on post code and the $ Amount
10. When finding the Top Agents negative amount is also considered (as minimum loss) for that postcode
 
