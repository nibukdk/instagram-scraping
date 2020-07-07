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

![img]()

