# deleteTweetsPub


Hey everyone! I got this script from Quincy Larson's article on the freeCodeCamp Medium Page [read it here](https://medium.freecodecamp.org/how-to-delete-your-past-tweets-in-bulk-and-for-free-save-yourself-from-your-past-self-f8844cdbda2)
and that should take you through the steps on how to make this work. It's pretty simple, but in case you want a TLDR
version, here you go: 

1. Install the latest version of PIP (a Python package manager)

```
curl https://bootstrap.pypa.io/get-pip.py -o get pip.py
```
*Note: If you already have PIP installed you'll probably have to just upgrade it. I was running vers 9 and had to upgrade to
18.0. Just follow the error messages if you get any. You'll probably be ok if you're running an older version*

2. Request a copy of your past Tweets from your account. You can accomplish this by clicking on your profile
picture on Twitter, clicking on 'Settings and Privacy' and then at the bottom you'll see an option to get
"Your Tweet Archive". Select that and you'll receive your tweet archive in a .csv file. Download that and take
note where you put it. 

<img width="238" alt="screen shot 2018-08-26 at 10 34 55 pm" src="https://user-images.githubusercontent.com/2258709/44637769-18fe6280-a981-11e8-9df4-d3fd831056af.png">
<img width="135" alt="screen shot 2018-08-26 at 10 35 05 pm" src="https://user-images.githubusercontent.com/2258709/44637792-421ef300-a981-11e8-8777-f230190582c0.png">

3. [Sign up for a Twitter Developer Account](https://apps.twitter.com/app/new) and after some questions like "What's your
user name" and "What are you using the app for?" you'll be granted access to your own keys for the Twitter API. Click on 'Keys and Tokens'
on your Twitter Developer profile and you'll see your 'Consumer API' keys. You'll have to create your own access token as well, 
so be sure to click on that below your Consumer Key and Secret Keys. I put them in a .txt file so I could copy and paste them
into the code, and then deleted it. You can regenerate if they ever expire. 

4. Create a folder to store the repo, and go to that folder in your terminal.

```
cd delete-tweets
```

5. Clone the following [Github repo https://www.github.com/QuincyLarson/delete-Tweets.git](https://www.github.com/QuincyLarson/delete-Tweets.git)

6. Open your text editor and open ```deletetweets.py``` from the repo. 

7. Go to line 54, and paste in your API keys starting with your Consumer Key, then your Consumer Secret Key, etc. 

8. Remember when you requested that copy of your Twitter archive? 
Right now the repo you just cloned has a blank ```tweets.csv``` file, so you need to replace it with your own archive.
Unzip the file you got from Twitter via email, copy your ```tweets.csv``` file (a simple right click and copy from Windows Explorer
or Finder is fine) and paste it into your ```delete-tweets``` folder. 

9. Once that's done, you're ready to run your file. First decide what you want your 'cutoff date' to be. 
If you want to delete all the tweets before 2016, you'll set December 31, 2016 as your cutoff date. 
Go into your Terminal, and run your file by typing ```python deleteTweets.py -d 2016-12-31```
and it will be off to the races.

![image](https://user-images.githubusercontent.com/2258709/44638212-acd12e00-a983-11e8-98b2-c8740460d9ab.jpeg)

Should be a good fun project for anyone experimenting with API's, or just wanting to control their Twitter feed. Thanks, and enjoy!

