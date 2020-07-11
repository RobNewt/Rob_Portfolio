# About me

I love math, coding, and data. Since finishing my phd in algebraic topology (2013) I've been teaching high school math. I started to integrated more coding into my teaching 5 years ago and have not looked back! I've introduced entire grades of students to Jupyter notebooks, led a calculus class to implement gradient descent and solve regression problems, watched students implement k-means from scratch to compress images, and most recently led an independent study on image classification with deep learning.

Here are some of my own projects. Tools I use include Python, Jupyter notebook, Google Colaboratory, NumPy, pandas, scikit-learn, Keras, TensorFlow and others.


 
## 1. Billboard Hot 100 with Spotify Audio Features [the code](https://github.com/RobNewt/Data-Analysis/blob/master/Billboard_Top_100.ipynb)

Since 1958, Billboard Magazine publishes a weekly chart of the hottest 100 songs in music based on sales, radio play, and streaming. I did some EDA on this data set to look at trends over time.

Each song has a number of weeks it's been on the Hot 100 so far (this increases by 1 each week the song is on the chart). By fixing a chart and averaging the number of weeks each of that chart's songs have been on the charts, I get an average number of weeks for songs on that particular chart. I plotted that over time and noticed on average songs are staying longer on charts. Note that there is an initial lag as the average number of weeks on chart for songs on the first chart was 1... it was the very first chart!

![Average Weeks per song](/Billboard 100 Images/AvgWeeksPerSong.png)

To further refine that view, this is the same average but applied to the bottom 50 songs of each chart.

![Average Weeks per song](/Billboard 100 Images/Bottom50Songs.png)

At some point in the 90s, it looks like there was a pretty movement towards less popular songs staying on the charts longer.

Furthermore, Spotify has an API that extracts audio features from a song, including duration, energy, danceability, loudness, etc. A full description is available at (https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/)

Audio Features for Billboard Hot 100 songs are available, so I looked at how some of those features have changed over time. 

For example, this is how the average length of top 100 songs has changed over time.

![Average Song Length per weekly chart](/Billboard 100 Images/LengthOverTime.png)

Before building any models, I needed to investigate the features a bit more. I suspected some correlated, like energy and danceability, so I first looked at correlation between these features.

![Correlation Heatmap](/Billboard 100 Images/AudioCorrelarity.png)

From there, I cleaned the data, applied a minmax scalar, and built 5 models: multiple linear regression, boosted linear regression, decision tree, random forest, and sequential neural network.

The multiple linear regression model was clearly the worst. The comparison of the other 4 was trickier. In some ways the decision tree was the strongest.

Below is the kde for each model, in some rough sense, a smoothed out histogram using probability rather than actual counts.

![Correlation Heatmap](/Billboard 100 Images/modelcomparison.png)

I looked up some of the songs that were the worst classified to see where my models failed.

Last I integrated Spotify's api into the workbook so I could grab audio features for any song I was interested in and see what my models would predict as the age of that song.


## 2: Rolling Stone's Top 500  [the code](https://github.com/RobNewt/Data-Analysis/blob/master/Rolling%20Stone's%20Top%20500%20(EDA).ipynb)

  This project is an exploration of Rolling Stones top 500 albums of all time. I looked at the breakdown by genre and over time. There's a lot of Rock, and a lot of it comes from 1970-1980! 
