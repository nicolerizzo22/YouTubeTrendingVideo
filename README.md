![youtube_image_for_readme](https://github.com/user-attachments/assets/7dcef74a-3396-47bc-ac23-8793f597f4e4)

## YouTube Trending Video Data Collection & Analysis with Python

In this project, I’ll take you through the task of YouTube data collection and analysis using Python in order to analyze the top trending videos and find what makes a video trend on YouTube (results reflect query date 12/18/24). 

I used the YouTube Data API to fetch details of the top 200 trending videos in the US, iterating through the API's paginated responses to collect **video details** such as:
- title
- description
- published date
- channel information
- tags
- duration
- definition
- captions

And various **engagement metrics** such as:
- views
- likes
- comments

The script will compile this information into a list, and then convert it into a pandas DataFrame.  We'll save the data to a CSV file named `trending_videos.csv`, allowing analysis of trends and patterns in the collected video data.


| Objective | Outcome |
| ---------------------------------------                                   | --------------------------------------------------------------------------------------- |
| Review Missing/incomplete/NULL values & data types                        | `published_at` needs to be changed from object to datetime data type  |
| Review descriptive statistics                                             | _normal_
| Review distribution of  _likes, views_ and _comments_ with a histogram    | Results show the distribution to be right-skewed, with most videos having lower counts and a few videos having very high counts |
| Review correlation between _likes, views_ and _comments_ with a heatmap   | Heatmap confirms strong positive correlations between views, likes, and comments |
| Review category counts for trending videos and visualize with a bar chart | It shows that Gaming, Entertainment, Music & Sports are the categories with the highest number of trending videos |
| Review average engagement metrics by category                             |  **Film & Animation** have the highest number of likes and comments, while **Science & Technology** has the highest view count by category | 
| Analyze the content and duration of the videos (convert duration from ISO 8601 to seconds using `isodate` library) after conversion, categorize the videos into duration range buckets by creating a new column called `duration_range` | Videos in the 0–5 minute range have the highest average view counts, likes, and comments. Engagement decreases as video length increases |
| Analyze relationship between views and number of tags used in the video with a scatterplot |  Scatterplot shows a very weak relationship between the number of tags and the view count, suggesting that the number of tags has minimal impact on a video’s view count |
| Analyze the time the video is posted and if there is any impact on views, extract the hour of publication, create a bar chart to reflect the distribution of `publish_hour` | Distribution shows most videos are published between 16:00 - 17:00 (4 PM- 5 PM), indicating an optimal time to upload |
| Analyze the relationship between publish hour and view count with a scatterplot | Weak negative relationship between publish hour and view count, suggesting that the hour of publiction has minimal impact on engagement metrics



#### Visuals
- Histogram
- Heatmap
- Scatterplot
- Bar Chart

### Conclusion:

####  ![trend_image3](https://github.com/user-attachments/assets/32c1ba3c-301f-493e-bf80-941b516a0c45)  Here are some key takeaways on what makes a video trend on YouTube:


- Encourage viewers to like and comment on videos to boost engagement metrics.
- Aim to create shorter videos (under 5 minutes) for higher engagement, especially for categories like Music and Entertainment.
- Schedule video uploads around peak times (4 PM — 5 PM) to maximize initial views and engagement.
