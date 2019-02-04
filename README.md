# feeds

## Instagram

### Getting Started - Client-side (Implicit) Authentication
Login to Instagram. 

Visit https://www.instagram.com/developer/clients/manage/ and register a new client.

1. Redirect to authorization URL:
https://api.instagram.com/oauth/authorize/?client_id=CLIENT-ID&redirect_uri=REDIRECT-URI&response_type=token

*Note:* Copy redirect_uri parameter from client management area under the Security tab. It is important to copy it exactly as is. Also, you need to ensure Disable implicit OAuth checkbox is unchecked.

2. Receive access_token via URL fragment
You will then be redirected to the redirect uri with the access token fragment.

http://your-redirect-uri#access_token=ACCESS-TOKEN

Grab access token off the URL.

### Using this Resource
1. Modify the js/config.js file to include your access token and the number of photos you want to display.
2. JQuery is required for the ajax call. Make sure it is initialized before calling js/igfeed.js.
4. After jQuery is loaded, insert this script:
`<script type="text/javascript" src="js/config.js"></script>`
3. Include js/igfeed.js in your code after config.js:
`<script type="text/javascript" src="js/ajax.js"></script>`
4. To insert the feed, add `<ul id="igfeed"></ul>`

*TODO:* We need a way to include config.js directly into igfeed.js for simplicity.