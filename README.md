Setup
=====

You will need:

* Scala 2.10+
* Play Framework
* MongoDB

Download the food review file (500K reviews) using the `download.sh` script.

Running the example
===================

    $ play package run



WorkFlow 
===================
application - recommender: 

getRamdomProduct: Rondomly pick up from the review file for the user to rate,
parse display the random product page with retries 

get the user's rating 
ratingCollection save the rating to with async and promise 

recommmender.Async recommendation
get the user rating from the database 
get amazon user rating  
get model recommender.predict(
	myrating, 
	amazonRating, 
	model = ALS.train(partition, 10, 20, 0.01).collect()
)

