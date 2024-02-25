# Productivity Guardian Chrome Extension

This is a Chrome extension that helps you stay productive by blocking distracting websites.

## Files

### contentScript.js

This script runs in the context of the web page. It listens for messages from the popup script to start a timer. When the timer expires, it alerts the user and sends a message to the background script to close the tab. It also checks if the current URL is in the list of blocked URLs and if so, closes the tab.

### popup.js

This script runs in the context of the popup. It gets the URL of the current tab and displays it in the popup. It also listens for clicks on the "BLOCK THIS URL" button. When the button is clicked, it checks if the URL is already blocked or in the process of being blocked. If not, it adds the URL to the list of blocked URLs in local storage and sends a message to the content script to start a timer. When the timer expires, it changes the status of the URL to "BLOCKED".

### popup.html

This is the HTML for the popup. It includes a title, a display area for the current URL, a "BLOCK THIS URL" button, and an area for displaying error messages.

## Usage

1. Open the popup by clicking on the extension icon.
2. The current URL will be displayed in the popup.
3. Click the "BLOCK THIS URL" button to block the current URL.
4. If the URL is already blocked or in the process of being blocked, an error message will be displayed.
5. If the URL is not already blocked, a timer will start. When the timer expires, the URL will be completely blocked for the rest of the day.
