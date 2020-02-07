# Under the Spell

A simple spelling learning app for kids build using LG WebOS SDK for LG TVs. 
This app has two text input fields
 - Reference text input field to be used by teacher / adult
 - Practice input field to be used by learner / kid
![Under the Spell]([https://github.com/ashok2ashok/UnderTheSpell/screenshots/Right.png](https://github.com/ashok2ashok/UnderTheSpell/screenshots/Right.png))
## Process
Follow the below steps to get most value out of this app:
 1. Type the word/spelling you want to teach in the **Reference** text field
 2. Press Down button on the Remote / Tab on the keyboard to **switch focus to the Practice field**.
 3. Give the Remote / Keyboard to the learner/kid and ask him/her to watch the word in the reference field and **type it in the practice field**. Note that you can't type more than about 1 letter per second as this **field is throttled**. 
 4. Once it's typed, press OK on remote / Enter on Keyboard. Both reference field and practice **fields are compared**. Comparision is case-insensitive. 
	 5. If the words don't match, then an **error message is dispayed** with image
	 6. If the words match, then a picture from the **first google image search** result. for that word is displayed on the right.

Note: Use a wireless keyboard connected to the TV / device for a better experience

## Technical Details

### Google Custom Search API Key
For this app to work, Google Custom Search API Key needs to be configured in the file `script/credentials.js`. Create this file or rename and update the file `script/credentials-template.js`

Get the API Key from the following link: 
https://developers.google.com/custom-search/v1/overview

Paste it in the below line:
`var MY_SEARCH_API_KEY = "<YOUR_API_KEY_HERE>";`

### Key Throttling in the Practice field
Typing speed is throttled to about 1 key per second. I put this in after my kid had trouble typing the letters on the keyboard resulting in multiple repeated characters and deletes when he pressed backspace. You can update this by configuring the below variable in `index.html`
`var KEY_THROTTLE_MILLISECS =  800;`

### Implementation
Used jQuery in this app. All the logic is present in `index.html`

### Images used in the app
All the images used in the app are royalty free

