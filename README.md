![youtube_image_for_readme](https://github.com/user-attachments/assets/7dcef74a-3396-47bc-ac23-8793f597f4e4)

## YouTube Trending Video Data Collection & Analysis with Python

In this project, I’ll take you through the task of YouTube data collection and analysis using Python in order to analyze the top trending videos and find what makes a video trend on YouTube (accurate as of 12/18/24). 

To collect data from YouTube, you need to set up an API. After that key has been generated, we can proceed to data collection, where we want to gather data about the top 200 trending videos on YouTube. 

In the first cell of code, we're using the YouTube Data API to fetch details of the top 200 trending videos in the US, iterating through the API's paginated responses to collect video details such as title, description, published date, channel information, tags, duration, definition, captions and various engagement metrics such as views, likes and comments. The script compiles this information into a list, converts it into a pandas DataFrams and saves the data to a CSV file named `trending_videos.csv`, allowing us to analyze trends and patterns in the collected video data.

Next, we want to take a look at the missing values (if any) and data types. The data types seem appropriate for most columns, but we may need to convert the `published_at` column to a datetime format and tags might need further processing. We also want to take a quick look at the descriptive statistics. And finally, let's review the distribution of views, likes and comments of all the videos in the data. The histograms show that the distributions of view counts, like counts, and comment counts are right-skewed, with most videos having lower counts and a few videos having very high counts.

Next, it makes sense to take a look at the correlation between _likes, views_ and _comments_. The heatmap confirms strong positive correlations between views, likes, and comments.

In order to analyze the categories of the trending videos, we need to go back and get the category name (we didn't collect this data originally). After we've collected the category names, we can create a bar chart for cateogry counts of the top trending videos. 
It shows that Gaming, Entertainment, Music and Sports are the categories with the highest number of trending videos. 

Next, we want look at the average engagement metrics by category. **Film & Animation** have the highest number of likes and comments, while **Science & Technology** has the highest view count by category. 

Next, let's analyze the content and duration of the videos, to do that we will need to convert the duration from **ISO 8601** format (the global standard for date & time formats) to seconds using the `isodate` library.
After converting the durations, we are categorizing the videos into different duration ranges (0–5 minutes, 5–10 minutes, 10–20 minutes, 20–60 minutes, and 60–120 minutes) by creating a new column called `duration_range`.
This categorization enables us to analyze and compare the engagement metrics of videos within specific length intervals, providing insights into how video length influences viewer behavior and video performance.
Videos in the 0–5 minute range have the highest average view counts, likes, and comments. Engagement decreases as video length increases.

Now, let’s analyze the relationship between views and number of tags used in the video. First, we need to calculate the number of tags for each video. Then create a scatterplot with the tag count on the x axis and view count on the y axis. The scatter plot shows a very weak relationship between the number of tags and the view count, suggesting that the number of tags has minimal impact on a video’s view count.

Next, we will see if the time a video is posted has any impact on its views. First we will need to extract the hour of publication. Then we'll create a bar chart to show the distribution of publish hour. The distribution shows that most videos are published between 16:00 and 17:00 (4 PM - 5 PM), indicating this might be an optimal time for uploading videos. 
From the scatterplot we can see that there is a very weak negative relationship between publish hour and view count, suggesting that the hour of publication has minimal impact on engagement metrics.

### Conclusion:

####  ![trend_image3](https://github.com/user-attachments/assets/32c1ba3c-301f-493e-bf80-941b516a0c45)  Here are some key takeaways on what makes a video trend on YouTube:


- Encourage viewers to like and comment on videos to boost engagement metrics.
- Aim to create shorter videos (under 5 minutes) for higher engagement, especially for categories like Music and Entertainment.
- Schedule video uploads around peak times (4 PM — 5 PM) to maximize initial views and engagement.
