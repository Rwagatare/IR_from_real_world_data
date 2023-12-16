# Assignment 5: IR from Real Data
**Westmont College Fall 2023**

## Author Information
* **Name(s)**: Livingstone Rwagatare 
* **Email(s)**: lrwagatare@westmont.edu

## Introduction
In this project, I aimed to discover and analyze trends in my YouTube viewing activity. The dataset I used was my Youtube watching history downloaded from Google Takeout. The data file I processed was in JSON format. I performed data preprocessing, visualization and interpretation all in the same Python notebook. I made extensive use of the library Pandas which encapsulates some information retrieval techniques covered in the course such as indexing and query processing. I also utilized the libraries Seaborn and Matplotlib in creating visualizations of my viewing activity. Finally, I used the WordCloud library to create a word cloud based on the text in the video titles of all the videos in my watching history to identify key terms with the highest frequency.

## Project Structure
The project consists of two main components: Data Preprocessing, Data Visualization and Interpretation. Both compoments are implemented in the same notebook, analysis.ipynb.

## Implementation Details
### Data Preprocessing
Using pandas, I fit the raw JSON data into a dataframe. I then filtered out the ads watch history to retain only the videos watched history data. I removed columns I was not interested in, to retain only the columns: title, titleURL, channel, and time. I split the time column into year, month, day, dayName, date for more granular analysis later on.  The title of every video started with "Watched " so I removed that to not have this show up as the highest frequency word in the word cloud. I also removed entries that had null values in the  columns I was interested in. 

### Data Visualization and Interpretation
I performed 5 visualizations, 1 based on the text in the video titles and the other 4 based on time. The first visualization was a word cloud based on the video titles text. 4 of the time-based visualizations showed my viewing activity based on the time of day, the day of the week, the month of the year, and the year in the range 2017-2023. The 6th visualization was a heatmap for a week showing both days of the week and the time of day. 
From this visualization, I could tell at different time scales, the times when my viewing activity was at its peak. From the word cloud, I could tell that the majority of my viewing activity was music-related as expected. 

### Reflections and Learning Outcomes
Through this project, I gained new skills in using the pandas and seaborn libraries. A future improvement I could make is identify the video categories for each video using the Youtube Data API, to track the changes in the Youtube genres I watch over different timescales. I ended up having to rely on libraries to encapsulate some of the information retrieval techniques because I was pressed for time, but I would have learned some more directly implementing the techniques such as implementing the vector space model to measure similarity in viewing patterns over different time periods using cosine similarity as a metric. This would use up a lot memory and processing power, so I would have needed to use cloud computing resources to do the same analyses. Doing this project has given me an appetite for carrying out analyses on personal data accrued over time. I look forward to experimenting with the rest of my Google data and other available data from social media apps. 

