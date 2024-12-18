![youtube_image_for_readme](https://github.com/user-attachments/assets/7dcef74a-3396-47bc-ac23-8793f597f4e4)

## YouTube Trending Video Data Collection & Analysis with Python

YouTube is a great place to help aid in the learning journey for both Data Analysts and Data Scientists. 

In this project, I’ll take you through the task of YouTube data collection and analysis using Python in order to analyze the top trending videos and find what makes a video trend on YouTube. 

To collect data from YouTube, you need to set up an API. After that key has been generated, we can proceed to data collection, where we want to gather data about the top 200 trending videos on YouTube. 

In the first cell of code, we're using the YouTube Data API to fetch details of the top 200 trending videos in the US, iterating through the API's paginated responses to collect video details such as title, description, published date, channel information, tags, duration, definition, captions and various engagement metrics such as views, likes and comments. The script compiles this information into a list, converts it into a pandas DataFrams and saves the data to a CSV file named `trending_videos.csv`, allowing us to analyze trends and patterns in the collected video data.

Next, we want to take a look at the missing vales (if any) and data types. The data types seem appropriate for most columns, but we may need to convert the published_at column to a datetime format and tags might need further processing. We also want to take a quick look at the descriptive statistics. And finally, let's review the distribution of views, likes and comments of all the videos in the data. The histograms show that the distributions of view counts, like counts, and comment counts are right-skewed, with most videos having lower counts and a few videos having very high counts.

Next, it makes sense to take a look at the correlation between likes, views and comments. The heatmap confirms strong positive correlations between views, likes, and comments.

Now we want to analyze the categories of the trending videos and we need to go back and get the category name. After we've collected that information, we can create a bar chart for cateogry counts of the top trending videos. 
It shows that Gaming, Entertainment, Music and Sports are the categories with the highest number of trending videos. 

Next, let's look at the average engagement metrics by category. 

