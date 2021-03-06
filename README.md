# NotificationManager Plugin

Written by Abraham Walters<br>
* v1.0 - July 2011
* v1.1 - July 2012

This plugin extends the Font class and allows you to  move it and have
it fade after a specified amount of time. The plugin also provides a 
NotificationManager to do all your dirty work and track each Notification 
for updating and drawing.

To use the plugin you will need to create an instance of the
NotificationManager in your game like so:
```javascript
myNoteMgr: new NotificationManager(),
```
You will then need to add myNoteMgr.update() to ig.game.update()
and myNoteMgr.draw() to ig.game.draw().  Make sure you add 
myNoteMgr.draw() after the this.parent() draw, otherwise your 
Notifications will be drawn over. From there you can spawn a
Notification within any Entity using the following syntax:
```javascript
ig.game.myNoteMgr.spawn('media/font.png', 'string', x, y, settings);
```
Or you can create a Notification and then feed it to the NotificationManager
later:
```javascript
var note = new Notification( 'media/font.png', 'string', x, y, settings );
//other code
ig.game.myNoteMgr.add( note );
```
The NotificationManager also provides find() and remove() methods for managing
your notifications. You can also use Notifications sans the NotificationManager.
Feel free to dig into the code and the changelog for more details.

Enjoy!