# About me

I love math, coding, and data. Since finishing my phd in algebraic topology (2013) I've been teaching high school math. I started to integrated more coding into my teaching 5 years ago and have not looked back! I've introduced entire grades of students to Jupyter notebooks, led a calculus class to implement gradient descent and solve regression problems, watched students implement k-means from scratch to compress images, and most recently led an independent study on image classification with deep learning.

Here are some of my own projects. Tools I use include Python, Jupyter notebook, Google Colaboratory, NumPy, pandas, scikit-learn, Keras, TensorFlow and others.

 
### 2. Billboard Hot 100 with Spotify Audio Features (EDA + Classification) [the code](https://github.com/RobNewt/Data-Analysis/blob/master/Billboard_Top_100.ipynb)

Since 1958, Billboard Magazine publishes a weekly chart of the hottest 100 songs in music based on sales, radio play, and streaming. I did some EDA on this data set to look at trends over time.

Each song has a number of weeks it's been on the Hot 100 so far (this increases by 1 each week the song is on the chart). By fixing a chart and averaging the number of weeks each of that chart's songs have been on the charts, I get an average number of weeks for songs on that particular chart. I plotted that over time and noticed on average songs are staying longer on charts.

![Average Weeks per song](/Billboard 100 Images/AvgWeeksPerSong.png)

To further refine that view, this is the same average but applied to the bottom 50 songs of each chart.

![Average Weeks per song](/Billboard 100 Images/Bottom50Songs.png)

At some point in the 90s, it looks like there was a pretty movement towards less popular songs staying on the charts longer.


Project 1: Rolling Stone's Top 500 

  This project is an exploration of Rolling Stones top 500 albums of all time. I looked at the breakdown by genre and over time. There's a lot of Rock, and a lot of it comes from 1970-1980! 
