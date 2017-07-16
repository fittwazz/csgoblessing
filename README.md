# csgoblessing

What is this?

CSGO Win Big is a Counter-Strike: Global Offensive jackpot skin betting website, created by me, Jordan Turley. It is no longer hosted, but you can view images of the site here, or download and inspect the code yourself.

How does CSGO Win Big work?

This is the repository for the website for CSGO Win Big. It is written in HTML/CSS/JavaScript for the client-side, and PHP for the server-side.
We are also making use of the following libraries/frameworks:

jQuery - http://jquery.com/
Bootstrap - http://getbootstrap.com/
Underscore.js - http://underscorejs.org/
SweetAlert - http://t4t5.github.io/sweetalert/
SteamAuthentication - https://github.com/SmItH197/SteamAuthentication
In addition to the website, we are also making use of a custom version of Jessecar96's Steam Bot, which can be found here, and is written in C#.

How to setup this project for my own use?

If you would like to setup this project for your own project, there are a couple of steps you must follow:

In src/php/default.php, you must configure your own database credentials. The way I have it setup is I have a file outside of the web root with my passwords in it, called 'passwords.txt', which I read and get the password for the database from, instead of writing my password directly in the code. Then, import database-config.sql to your MySQL database. If you want to use a database other than MySQL, you will have to set it up on your own.
Also, because you login through Steam for this site, you must have a Steam API Key. You can request a key for yourself here. Like the database password, I also have this key stored outside of the web root in passwords.txt.
You will also have to put in your own website url and database stuff in some places, instead of mine. These places are:
Lines 5, 6, and 7 of default.php
Line 14 of settings.php
Line 30 of support-ticket.php
Line 6 of bot-withdraw.php. For this, you will need to enter the 64bit ID of your Steam bot. You can find this in the bot's profile url, or on websites such as http://steamrep.com.
Lines 54 and 120 of index.html, line 106 of support.html, line 92 of donations.html, and line 158 of prices.html. Here, you must modify the sign in url to have your own website's url. You must change where it says 'openid.return_to=' and 'openid.realm=' to be your own website's url.
Line 141 of script.js. Here, you must put in the trade url of your own bot.
One last thing, the site assumes that there will always be chat messages, so you have to manually insert one chat message into the chat database table.
Here is an example of my passwords.txt:
{"default-password":"YOUR DATABASE PASSWORD","steamAPIKey":"YOUR STEAM API KEY"}
How can I contribute to this project?

Please read CONTRIBUTING.md.

How can I donate to this project?

Donations are not necessary, but are greatly appreciated and help us out a lot. There are four ways you can donate:

Send a trade offer here with skin donations.
Send actual money through PayPal here.
Send Bitcoin to this address: 1GqszRekcjuUTARfXiroMnPoytRJWdk66A
Send Dogecoin to this address: DMWd9PLkDyQqEaQnoCWHi8EFDv2biD4AcS
If you are sending skins or money through PayPal, and would like to be recognized for your donation on our donations page, please add your name to the trade offer message or field on PayPal.
 
