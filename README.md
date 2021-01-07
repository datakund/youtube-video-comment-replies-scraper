## Youtube-Video-Comments-Replies-Scraper
A python library that uses browser automation to scrape replies of commnents on youtube videos
It uses [datakund](https://pypi.org/project/datakund) internally

Complete Documentation available [here](https://youtube-api.datakund.com/en/latest/)


### Support
For any help / feedback you can message us here
* datakund@gmail.com
* https://t.me/datakund

### Installation

```sh
pip install youtube-video-comment-replies-scraper
```

### Import

```javascript
from youtube-video-comment-replies-scraper import *
```

### Open Video

To open video we use ``open`` function
It requires **url** as input parameter

```javascript
youtube.open("place_video_url_here")
```

### Scroll page with Keypress

To bring comments section into view we scroll down the page using ``keypress`` method
This function requires **key** as input parameter
We pass **pagedown** as input 

```javascript
youtube.keypress("pagedown")
```

### Find comment by text & click View Replies button

To show replies of particular comment we first find the comment by its text then click on view replies button
We acheive this using ``click_view_replies`` method
It requires **comment** as input parameter

```javascript
youtube.click_view_replies(comment="comment_text_here")
```

### Click Show More Replies button

To show more replies of particular comment we use ``show_more_replies`` method
It does not require any input parameter

```javascript
youtube.show_more_replies()
```

### Fetch Replies

To fetch all replies on current page we use ``get_comment_replies`` method
It does not require any input parameter
It will try to fetch all replies opened on page in browser

```javascript
response=youtube.get_comment_replies()
replies=response['body']
```

### Example Response

```sh
[
   {
      "userlink":"userlink",
      "replytext":"replytext",
      "user":"user"
   },
   {},
   ...
]
```

### DataKund
It uses [datakund](https://pypi.org/project/datakund/) internally to do browser automation
DataKund is an automation library that uses selenium & supports automation of many sites including [Youtube](https://youtube-api.datakund.com/en/latest/), [Amazon](https://amazon-api.datakund.com/en/latest/), [Twitter](https://twitter-api.datakund.com/en/latest/), [LinkedIn](https://linkedin-api.datakund.com/en/latest/) , [Google](https://google-api.datakund.com/en/latest/) etc.
