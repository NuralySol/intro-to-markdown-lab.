# This is Nuraly Cookie Baking tutorial

## Steps to prepare for cookie making

1. To make a Cookie you need not that many ingredients and most ingredients are ready at home

2. Buy flour, yeast, and get available water and some chocolate pieces.

## The style that I have chosen is explained here

> i have set the style basic with neutral color using hexcode for the background 

```css
 this is the back ground color was used #f4f4f4; 
 ```
### This is the rest of code of styles.css file
This code snippet sets the style of the index.html consistent.
```css
h1 {
    color: #333;
}

p {
    color: #666;
}

.container {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    text-align: center;
}
```
### What is in the code you might as that runs this website?

* The function set a cookie

```javascript
function setCookie(name, value, days) {
    const d = new Date();
    d.setTime(d.getTime() + (days*24*60*60*1000));
    const expires = "expires="+ d.toUTCString();
    document.cookie = name + "=" + value + ";" + expires + ";path=/";
}
```

* This function gets the cookie
```javascript
function getCookie(name) {
    const nameEQ = name + "=";
    const ca = document.cookie.split(';');
    for(let i=0; i < ca.length; i++) {
        let c = ca[i];
        while (c.charAt(0) === ' ') c = c.substring(1, c.length);
        if (c.indexOf(nameEQ) === 0) return c.substring(nameEQ.length, c.length);
    }
    return null;
}
```
* This function checks for a cookie

```javascript
function checkCookie() {
    const user = getCookie("username");
    if (user !== null) {
        alert("Welcome again " + user);
    } else {
        const username = prompt("Please enter your name:", "");
        if (username !== "" && username !== null) {
            setCookie("username", username, 365);
        }
    }
}

window.onload = checkCookie;
```

![This is an image of a cookie](https://images.unsplash.com/photo-1499636136210-6f4ee915583e?q=80&w=2678&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)