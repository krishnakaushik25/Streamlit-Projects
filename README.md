## The Magic of Streamlit

The only way to truly understand how magical Streamlit is to play around with it. But if you need to be convinced first, then here is the **4 minute introduction** to Streamlit!

Afterwards you can go to the [Streamlit docs](https://streamlit.io/docs/) to get started. You might also visit [Awesome Streamlit docs](https://awesome-streamlit.readthedocs.io/en/latest/).

[![Introduction to Streamlit](https://github.com/MarcSkovMadsen/awesome-streamlit/blob/master/assets/youtube-introduction-to-streamlit.png?raw=true)](https://www.youtube.com/watch?v=B2iAodr0fOo&feature=youtu.be "Introduction to streamlit")

I’ve been playing around with streamlit and I am extremely impressed by it.

It’s fast, responsive, and is very easy to get a grip on.In my opinion, working with streamlit is quite enjoyable. We can deploy our streamlit application on Heroku as well to show it to the world.

What files you need for deployment on heroku of a streamlit application?
There are four essential components required to launch your streamlit application on Heroku.

setup.sh
requirements.txt
Procfile
your_application.py

setup.sh — no credentials needed
Note: You do not need to name this file exactly setup.sh, it can be anything however it needs to end with an .sh file extension. However, naming it setup.sh seems to be the norm.

```
mkdir -p ~/.streamlit/

echo "\
[general]\n\
email = \"your-email@domain.com\"\n\
" > ~/.streamlit/credentials.toml

echo "\
[server]\n\
headless = true\n\
enableCORS=false\n\
port = $PORT\n\
" > ~/.streamlit/config.toml

```

requirements.txt - This file essentially lists all the specific python plugins we will use in our streamlit application.

Procfile
Note: Name this file as Procfile, do not put any extensions after it. It is a standard text file.
```
web: sh setup.sh && streamlit run your_application.py
```
And after this files, we can create a new heroku app by using Heroku CLI or pushing it to github and using it for share.streamlit.io.

share.streamlit.io needs only requirements.txt file and your_application.py file.(Thats' it)

## Streamlit Apps:

These are some of the applications I built using streamlit.


+ [Image detection with FastAPI using Amazon ec2](https://github.com/krishnakaushik25/fastapi-opencv)
+ [Wiki Text-to-Voice App](https://github.com/krishnakaushik25/WIKI-Text-Voice)
+ [Streamlit Style Transfer App](https://github.com/krishnakaushik25/streamlit-style-transfer)
+ [Streamlit dashboard contains Twitter cashtags and StockTwits](https://github.com/krishnakaushik25/streamlit-twitter-StockTwits)
+ [Category classification for news - News Classifier](https://github.com/krishnakaushik25/NLP-news-classifier)
+ [Face detection, which includes eye detection, cartonize, and cannize images](https://github.com/krishnakaushik25/face-detection-opencv-streamlit)
+ [NLP tasks - Sentiment Analysis, Named Entity Recognition (NER), and Text Summarization](https://github.com/krishnakaushik25/NLP-Tasks-Streamlit)
+ [Movie recommender system](https://github.com/krishnakaushik25/movie-recommender-streamlit)
+ [Cryptocurrency prices](https://github.com/krishnakaushik25/Streamlit-Crypto-webapp)
