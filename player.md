# Embedded audio player

When REELRADIO was launched in 1996, the site used Real Audio 2.0 to stream the exhibits.
When our client took over the administration of the site the exhibits were converted to m4a and VLC player was used to play the exhibits.
While this allowed most of the subscribers to play the exhibits successfully, the client wanted to implement an embedded player to the site.

Now, the site contains hundreds of collections, each of which is an HTML file with links to play the exhibits.
So, instead of rewriting all of the links by hand, we dynamically add an on click function via JavaScript when the page loads.
This functions calls another PHP file that requests the exhibit and returns a URL to the stream engine.

Our team decided to use the [Plyr.js](https://github.com/sampotts/plyr) player because of its ability to be styled to match the aesthetic of the site.
The player itself persists while the user is still able to browse around the site.
We achieved this via a combination of `iframe`s and CSS styling.
