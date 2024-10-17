# web-phone

## Getting Started with Phone.com Web Phone
This is an early version of the phone.com web phone that can be embeded in any website. It will bind to an html id of either `webPhoneRoot` xor `root`

Add the following to your web page and the web phone will load.
```
<div id="webPhoneRoot"></div>
<script src="https://preprod.web-phone.apps.phone.com/2024.10.17@d3de342/index.js"></script>
```
Note: it will request users login to phone.com if a sessino is not already set. 
This has not yet been tested on non phone.com domains. CORS errors could occur on some fetches. You may need to contact phone.com to have extepect domains added to cors response. 

## Available example

In the example directory, you can run:

### `npm run start-https`

Runs the app in the development mode.\
Open [https://localhost:3000](https://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

