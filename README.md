# page-shield
AKA really bad security for web pages. Don't use this. Seriously. It's not a substitute for real authentication and encryption. It's a proof-of-concept.

This solution might stop casual users from viewing your page content, but it can easily be bypassed by anyone with a rudimentary knowledge of javascript, html, or even using a browser's built-in page inspection tools. Do not use it to protect confidential or proprietary information!

## how to use
Copy the `page-shield.js` file to your own web server, then add a `<script>` element within the `<head>` section of your web page source code which points to your copy, similar to the following:

```
<script type="text/javascript" src="page-shield.js"></script>
```

Adding this should mask out the content of your web page, and display a password prompt. When a valid password is entered, the prompt disappears and the main web page content is revealed. You must create at least one password file (see below) in order to allow visitors to view your content.

Multiple passwords are supported.

## managing passwords
Each password is stored as a separate file on your web server. The contents of each file are irrelevant as far as password validation is concerned, so you can store information in it if you like, such as the names of the people you have given that password to, or a password hint. Do not save the original password in this file!

### creating a password
Creating a password is as simple as using the [generator](http://technickle.github.io/page-shield/generate-hash.html), which will give you a filename based upon the password you entered.

### deleting a password
Simply delete the relevant password file on the web server. Once the file has been removed, that password will no longer work.

## Compatibility info
This has been tested on very basic web pages using both Safari and Chrome.

