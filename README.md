# Impact of 2022 US elections on social media

* The project has two parts, 1) Data collection from political subreddits on Reddit and 2)Data analysis (Topic analysis, Sentiment and Emotion Analysis) and visualization.


## Tech-stack - Reddit
* `python` - The project is developed and tested using python v3.9.7. [Python Website](https://www.python.org/)
* `time` - Time is a module that provides various time-related functions [Python Website](https://docs.python.org/3/library/time.html)
* `json` - Json enables users to work with a lightweight data interchange format JSON (JavaScript Object Notation) [Python Website](https://docs.python.org/3/library/json.html)
* `requests` - Requests is an HTTP library for Python. [Requests Website](https://requests.readthedocs.io/en/latest/)
* `pymongo` - PyMongo is a Python distribution containing tools for working with MongoDB [Pymongo Website](https://pymongo.readthedocs.io/en/stable/)
* `Jupyter` - Jupyter is an open-source IDE and web application that you can use to create and share documents that contain live code, equations, visualizations, and text [Jupyter](https://jupyter.org/)
* `MongoDB Community Server` - It offers a flexible document data model along with support for ad-hoc queries, secondary indexing, and real-time aggregations to provide 
   powerful ways to access and analyze your data. It also contains MongoDB Compass which is a GUI for MongoDB and an interactive tool for querying, optimizing, and analyzing your MongoDB data.
   The project's reddit's database and collection were stored locally in MongoDB Compass. 
   Download link: [MongoDB Community Server](https://www.mongodb.com/try/download/community)
* `urllib` - urllib is a package that collects several modules for working with URLs [Python Website](https://docs.python.org/3/library/urllib.html)
* `collections` - This module implements specialized container datatypes providing alternatives to Python’s general purpose built-in containers [Python Website](https://docs.python.org/3/library/collections.html)
* `datetime` - The datetime module supplies classes for manipulating dates and times. [Python Website](https://docs.python.org/3/library/datetime.html)
* `dateutil` - The dateutil module provides powerful extensions to the standard datetime module, available in Python. [dateutil Website](https://dateutil.readthedocs.io/en/stable/)
* `pytz` - pytz brings the Olson tz database into Python. [Python Website](https://pypi.org/project/pytz/)
* `itertools` - This module contains functions creating iterators for efficient looping [Python Website](https://docs.python.org/3/library/itertools.html)
* `numpy` - The fundamental package for scientific computing with Python [numpy Website](https://numpy.org/doc/stable/user/whatisnumpy.html)
* `NRCLex` - An affect generator based on TextBlob and the NRC affect lexicon [NRCLex Website](https://pypi.org/project/NRCLex/)
* `vaderSentiment` - VADER (Valence Aware Dictionary and sEntiment Reasoner) is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media. [vaderSentiment Website](https://github.com/cjhutto/vaderSentiment)
* `bokeh` - Bokeh is a Python library for creating interactive visualizations for modern web browsers. [bokeh Website](https://bokeh.org/)
* `tensorflow` - An end-to-end machine learning platform [vaderSentiment Website](https://www.tensorflow.org/)
* `keras` - Keras is a high-level, deep learning API developed by Google for implementing neural networks. [keras Website](https://www.tensorflow.org/)


## Data-source documentation

* `Reddit` - We are using `r/politics`, `r/news`, `r/democrats`, `r/Republican`, `r/conservative`, `r/worldnews`, `r/moderatepolitics`, `r/NeutralPolitics`, `r/progressive`, `r/PoliticalDiscussion`, `r/uspolitics`, `r/politics2`, `r/AmericanPolitics`, `r/Liberal`, `r/Republicans`, `r/conservatives`, `r/StateOfTheUnion`.
  * [r/politics](https://reddit.com/r/politics) - News and discussion about U.S. politics
  * [r/news](https://reddit.com/r/news) - News articles about current events in the United States and the rest of the world
  * [r/democrats](https://reddit.com/r/democrats) - The Democratic Party's daily news updates, policy analysis, links, and opportunities to participate in the political process
  * [r/Republican](https://reddit.com/r/Republican) - Partisan subreddit for Republicans to discuss issues with other Republicans
  * [r/conservative](https://reddit.com/r/conservative) - Subreddit for conservatives, both fiscal and social, to read and discuss political and cultural issues from a distinctly conservative point of view
  * [r/worldnews](https://reddit.com/r/worldnews) - A place for major news from around the world, excluding US-internal news.
  * [r/moderatepolitics](https://reddit.com/r/moderatepolitics) - Political subreddit for moderately expressed opinions and civil discourse
  * [r/NeutralPolitics](https://reddit.com/r/NeutralPolitics) - A heavily moderated community dedicated to respectful, empirical discussion of political issues
  * [r/progressive](https://reddit.com/r/progressive) - A community to share stories related to the growing Modern Political and Social Progressive Movement.
  * [r/PoliticalDiscussion](https://reddit.com/r/PoliticalDiscussion) - Subreddit for discussion about politics.
  * [r/uspolitics](https://reddit.com/r/uspolitics) - A subreddit for US Politics.
  * [r/politics2](https://reddit.com/r/politics2) -  place to discuss the American political process, the political parties, the politicians, political news and candidates.
  * [r/AmericanPolitics](https://reddit.com/r/AmericanPolitics) - A place to discuss the American political process, parties, the politicians and topics
  * [r/Liberal](https://reddit.com/r/Liberal) - A subreddit to discuss Liberal ideas including politics
  * [r/Republicans](https://reddit.com/r/Republicans) - Pro-Republican subreddit to discuss politics
  * [r/conservatives](https://reddit.com/r/conservatives) - Subreddit to discuss political ideas based on Conservatism 
  * [r/StateOfTheUnion](https://reddit.com/r/StateOfTheUnion) - A subreddit to discuss current political agendas and topics
  * The data contains posts  and comments of depth 1. The posts have been sorted based on the following
    * /new - New posts on subreddits
    * /hot - Posts gaining upvotes/comments on a rapid base
    * /rising - Newly submitted posts that's rapidly getting engagements
    * /top/?t=day - Top posts of the day
    * /top/?t=week - Top posts of the week
  * [Reddit API documentation](https://www.reddit.com/dev/api/) 
  * [Reddit API archive](https://github.com/reddit-archive/reddit/wiki/API)


## System Architecture for data collection

[System Architecture for Reddit](https://lucid.app/lucidchart/15df7844-7d98-4580-ae59-20332cc6ab97/edit?viewport_loc=-269%2C-31%2C2226%2C915%2C0_0&invitationId=inv_a9a04f58-5e94-44b8-8eb5-df7635da9bb6)


## How to run the project? - Reddit

#### Part 1 - Data Collection
Install `Python`, and [`MongoDB Community Server`](https://www.mongodb.com/try/download/community) to access `MongoDB Compass`

```bash
python3 -m pip install requests
python3 -m pip install pymongo
pip install jupyterlab
pip install notebook
```

Launch Jupyter Notebook using command prompt or the installed Jupyter Notebook App
```bash
jupyter notebook
```


* Create a Reddit account and then create an application to get application id and secret [Ouath2](https://github.com/reddit-archive/reddit/wiki/OAuth2)

* The textfile logininfo.txt contains login information of user
  * `Reddit username`, `password`, `application name`, `ápplication id`, `secret` each on new line in same order
  * The textfile subreddit.txt contains names of subreddits with one name on each new line
  * The textfile sorting.txt contains sorting parameter for posts on subreddit with one type on each new line

* Open the redditPart1.ipynb file
* For local MongoDB database, the the second cell must have `client = pymongo.MongoClient("mongodb://localhost:27017/")` or your mongoDB localhost link

* Run the redditPart1.ipynb jupyter notebook

#### Part 2 - Analysis
Installation of necessary libraries to run the project. Run the folliwing in OS command prompt/terminal or Anaconda prompt or run the code in Jupyter notebook
```bash
pip install NRCLex, vaderSentiment, bokeh, numpy, python-dateutil, pytz
pip install tensorflow
```
Launch Jupyter Notebook using command prompt or the installed Jupyter Notebook App
```bash
jupyter notebook
```

* Install the libraries and modules mentioned above
* Include the collected JSON data for posts ('postCollection.json') and comments ('commentCollection.json') in the same folder as the python notebook
* Open Jupyter Notebook App and locate the directory containing the python notebook and datasets
* Open the redditFinal.ipynb file
* Run the redditFinal.ipynb jupyter notebook
* The bokeh plotted graphs including an interactive graph with a dropdown for selection, will be displayed on new tabs.
* Some more graphs and text outputs will be displayed throughout the python notebook cells
(NOTE) Certain blocks of codes such as topic analysis on comments or emotion analysis of posts can take several minutes to execute and Emotion analysis of comments can take several minutes to couple of hours depending on the CPU specifications.

## Database schema - NoSQL

```bash

collection_2: redditDB.postCollection
{
  "_id": ObjectID,
  "subreddit": String,
  "postid": String,
  "created_utc": Double,
  "title": String,
  "selftext": String,
  "permalink": String,
  "num_comments": Int32,
  "upvotes": Int32,
  "upvote_ratio": Double,
  "url": String 
}

collection_3: redditDB.commentCollection
{
  "_id": ObjectID,
  "subreddit": String,
  "postid": String,
  "comment_id": String,
  "comment_text": String,
  "created_utc": Double
}
```
The reddit project has a database with two collections, one each for posts and comments

## Results

![pic1](https://user-images.githubusercontent.com/20452759/221375862-eceaeff2-0c01-48e5-9a94-4cd937d19ecc.JPG)
![pic2](https://user-images.githubusercontent.com/20452759/221375853-e5350a25-4b17-4b0d-a21b-c3ba1adbc152.JPG)
![pic3](https://user-images.githubusercontent.com/20452759/221375854-c042fa81-615c-4bd1-8252-2aefb3ce1c95.JPG)
![pic4](https://user-images.githubusercontent.com/20452759/221375855-64646294-0d7c-43e9-a0a3-9e683bd8a52c.JPG)
![pic5](https://user-images.githubusercontent.com/20452759/221375856-1e65834b-a07f-459f-8700-2b5acc9736ec.JPG)
![pic6](https://user-images.githubusercontent.com/20452759/221375857-f0c2ca14-53ba-48b1-9630-b26acab646a1.jpeg)
![pic7](https://user-images.githubusercontent.com/20452759/221375858-04cc212e-1a8c-4df9-bd4a-0af994e73282.jpeg)
![pic8](https://user-images.githubusercontent.com/20452759/221375859-1acff30e-7c44-4819-a0ac-396837aeb627.jpeg)
![pic9](https://user-images.githubusercontent.com/20452759/221375860-526e3e1f-17b2-4a55-8ccf-1fa14b781b73.jpeg)