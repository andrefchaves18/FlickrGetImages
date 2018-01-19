# FlickrGetImages
This App will use an API to Call Images from Flickr and display them randomly
Hi Udi,

Please appologize for the delay. Finaly i had the laptop setup with the tools i've found over internet (videos, blogs, etc).
I've used Expo XDE, Visual Studio Code, and before this i had to instal nodejs.

I've also created a dev account on Flickr to be able to have access to API Key.

So the process for this was:



1 - Created a folder to handle/store the main Index.js

2 - I've created 2 index.js (index.android.js and index.ios.js) to be able that every time i do a change on the main index it replicates on both 

Android and IOS.

The API Selected was the "flickr.photos.getPopular"

This is what is expected to be returned after the call:

{ "photos": { "page": 1, "pages": 1, "perpage": 100, "total": 100, 
    "photo": [
      { "id": "7510475868", "owner": "41704773@N04", "secret": "150169e267", "server": "8294", "farm": 9, "title": "st maurici Lake", "ispublic": 

1, "isfriend": 0, "isfamily": 0 },
      { "id": "6376654821", "owner": "41704773@N04", "secret": "521d187956", "server": "6106", "farm": 7, "title": "Hangers", "ispublic": 1, 

"isfriend": 0, "isfamily": 0 },
      { "id": "8387930671", "owner": "41704773@N04", "secret": "976b2beded", "server": "8370", "farm": 9, "title": "Waterfall", "ispublic": 1, 

"isfriend": 0, "isfamily": 0 }, ... etc....
)

3 - Changed from default name App to AppFlickr
"export default class AppFlickr"

4 - Description for User information. Just added a title.
<View style={styles.container}>
        <Text>Random Images From Flickr</Text>
      </View> 

5 - Created a new folder for API.js file called Utilities
	5.1 I've put the API inside of a variable
	
6 - API Call URL (With User ID and API Key)
	https://api.flickr.com/services/rest/?

method=flickr.photos.getPopular&api_key=842223564a15398f1cb603e8cd70e037&user_id=41704773%40N04&format=json&nojsoncallback=1&api_sig=f1230c73b04a43

8014a6c5dd254fb5d1

	6.1 Because my user ID didnt had any photos, i had to select a ramdom user with some photos to be available to the app.

7 - Implement the usage of an API
	"import api from './utilities/api';" into index.js


