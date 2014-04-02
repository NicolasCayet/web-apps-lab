
#Storage

With HTML5, web pages can store data locally within the user's browser via a new API : **Storage**. 
Earlier, this kind of feature was often done with cookies.

However, Web Storage is more secure and faster. The data is not included with every server request (as it works for cookies), but only used when asked for.

It's also possible to store large amount of data, without affecting the website's performances.

The data is stored in key/value pair. It can store only `string` as value (every types are cast as string).

###sessionStorage :

Values registered into a window are not found from another browser's window. Idem between two differents tabs into the same browser's window.

It allows to pass informations between differents pages through the same window and the same tab, without passing it into HTTP requests.

###localStorage :

Informations shared between every windows and every tabs of the same browser's type.

*i.e : value for a key stored in Chrome is not shared with value for this same key in Safari.*

BTW, everything else is possible with this module.

###Storage Event :
Listen for a `setItem` or a `removeItem` function call onto a `Storage` object within the same domain.

Can ONLY detect events fired from another tab or another window.

If the event was fired from the current page (in its tab from the current window) which is listening to 'storage' changes, it will not launch the associated function into this page.

Then : storage event is fired only for localStorage (because sessionStorage is available only for the current tab, it makes no sense to fire an event that nobody can catch).
