# Instagram Scraping

## Data Info

### Commands used to download files 

[Instaloader](https://instaloader.github.io/) was used for downloading the posts.Install the instaloader first to run this command. Run the following command  in command prompt. Fill the username section by your username of instagram, it will prompt from password in command prompt. 

The following command will download posts with hashtag "#workout" which is one of the most popular hashtags. 

### Installation
 One of the following
 - conda install instalaoder (its inside anaconda prompt)
 - pip install instaloader (recommended, beacuse u need to type password of insta)
 
### Command

$$instaloader --login=<username_instagram> --stories --highlights --no-profile-pic --no-pictures --no-compress-json --no-videos  --comments --geotags  --post-filter="date_utc >= datetime(2019, 5, 31)" --post-metadata-txt="{likes} likes, {comments} comments." --storyitem-metadata-txt=" {geotags} geotags. {stories} stories." "#workout"$$

### File types
Only post were used for this project but the command downloads four file variations with endings as follows:
- ..._UTC.json -> Files with all the info on post
- ..._UTC.txt -> FIles with info on just number of likes and comments
- ..._UTC_comments.json -> Files with comments on post
- ..._UTC_location.txt -> Files with location on the post

Only files ending on "_UTC.json"  were used in this project
    
### Columns used
From the files that returned json objects the following columns were chosen.
*The following columns are renamed and not as it is from the json file*

-  upload_format -> Uplaod Type, like image,video or sidecar
- likes_number -> NUmber of likes
- comments_number -> Number of Comments on the post
- address -> Address of the uploader
- owner_id -> User id of uploader
- owner_username -> Username of uploader
- product_type -> Type of post uploader like feed, igtv
- created_at -> Upload date in timestamp
- can_reshare -> Permisson to reshare the post
- able_to_comment -> Comments disabled or not


## Data time range

The data on #workout instagram post is available from 5th of January to 4th of July, 2020.

# Analysis

## Most uploaded Post Format

![img](https://github.com/nibukdk/instagram-scraping/blob/master/Imgs/Uploaded%20Format%20Portions.png)

Image is the most uploaded format followed by videos and sidecar respectively.

## Countries Ranking by Most liked videos

![img](https://github.com/nibukdk/instagram-scraping/blob/master/Imgs/Addresses%20by%20Like%20on%20Videos.png)

Australia takes top spot on most liked videos by countries, while Germany stands last, keeping on mind unkown addresses are not included.


## Ranking of Countries by Images likes
![img](https://github.com/nibukdk/instagram-scraping/blob/master/Imgs/Addresses%20By%20Images%20likes.png)

The address is given as yoga, which is probably the mention of pic doing yoga which has the most likes. And Canda,Kansas,Usa has the least likes from the tail display of image.


## Correlation Analysis
![img](https://github.com/nibukdk/instagram-scraping/blob/master/Imgs/Correlation.png)

There is high correlation between the two columns likes and comment numbers.

## User Popularity
 
![img](https://github.com/nibukdk/instagram-scraping/blob/master/Imgs/Avg%20Ranking%20Top%205%20users.png)

 The username *motihari_shootout* has only one post which has 5598 likes and 216 comments. The user *student_shubham* (from data)also has only one post, which is image that gained massive popularity with 1309 comments putting him/her at top for comments.

 ## Popularity by Upload Formats

### Popularity Based on Likes By Upload Format


![img](https://github.com/nibukdk/instagram-scraping/blob/master/Imgs/Users%20Likes%20By%20Upload.png)

 For image user *motihari_shootout* has most likes, while user *hada_eri* has most likes in sidecar formats and *nikalemusic* for video formats.


### Popularity By comments Based on Upload Formats

![img](https://github.com/nibukdk/instagram-scraping/blob/master/Imgs/User%20comments%20by%20Upload.png)


The result is similar to the result based on likes for video fomats. However, as far as top commented post by users on sidecar the winner is *garry626226* and *student_shubham* for most commented image uploading user.



## Most Active Users

![img](https://github.com/nibukdk/instagram-scraping/blob/master/Imgs/Most%20active%20users.png)

User by username "ka.the6661" has most post. Lets get into more details for this user. From Further analysis(check notebook), User seems to have uploaded all post in a day to be precise user has posted in about 30 min 44 posts.Since our data has limited timelines. Its not for sure if user is new user or has been recently active.Uploads of the data is from different places as well.