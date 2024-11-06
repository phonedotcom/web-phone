# web-phone

## Getting Started with Phone.com Web Phone
This is an early version of the phone.com web phone that can be embeded in any website. It will bind to an html id of either `webPhoneRoot` xor `root`

Add the following to your web page and the web phone will load.
```
<div id="webPhoneRoot"></div>
<script src="https://web-phone.apps.phone.com/2024.11.06@57938e/index.js"></script>
```
Note: it will request users login to phone.com if a session is not already set. 
This has not yet been tested on non phone.com domains. CORS errors could occur on some fetches. You may need to contact phone.com to have expected domains added to cors response. 

The bulk of the code example is found in the [public/index.html](https://github.com/phonedotcom/web-phone/blob/main/example/public/index.html) 
## Supported Fucntions


| window name               | type                    | Description |
| -----------               | -----------             | ----------- |
| window.WebPhoneHandler.maximizeWebPhone   | callback function       | function that will be called when the web phone wants to be maximized or in the forground, for example when there is an incoming call|
| window.WebPhoneHandler.minimizeWebPhone   | callback fucntion       | function that will be called when the web phone wants to be minimized, normally only when the minimize button is pressed|
| window.WebPhoneHandler.getLocalContacts   | called fucntion                | function provided by consumer page, allowing seaching of contact name given the entered phone number, this expects a return of a promise with a list `[{name: string, number: 'string', email: 'string', id: 'string'}]`|
| window.WebPhoneHandler.startCall   | fucntion                | function that will iniate the call on the web phone from the consumer page, ex: `window.WebPhoneHandler.startCall('+155555555555')`|



## Available example

In the example directory, you can run:

### `npm run start-https`

Runs the app in the development mode.\
Open [https://localhost:3000](https://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

