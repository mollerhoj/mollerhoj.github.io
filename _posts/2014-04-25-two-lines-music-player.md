---
layout: disqus
---
A two line music player for Mac OS X
=====

Today, I wrote a music player using Gary Bernhardts [selecta](https://github.com/garybernhardt/selecta), and UNIX.
Thank you, UNIX.

oh, and I made a new little demo, using the amazing showterm gem:
[Demo](http://showterm.io/18965b0e12b58a8f5cbe2)
Here is the code:

{% highlight bash linenos=table %}

#!/bin/sh
MUSIC_HOME="$HOME/Music/iTunes/iTunes Media/Music/"
open "$MUSIC_HOME$(find "$MUSIC_HOME" -type f | sed "s@$MUSIC_HOME@@g" | selecta -s $1)"

{% endhighlight %}

