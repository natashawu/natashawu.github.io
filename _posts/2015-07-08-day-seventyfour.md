---
layout: post
title:  "Day #74 - Prying"
---
We’ve been working on our capstones for a good couple weeks now and it’s been a lot of hard work, but pretty rewarding as well. For me, one of the most frustrating parts about creating my Rails app has been debugging. Throughout the course, we’ve learned how to use IRB and Rails console as tools for debugging. But to be honest, Rails console still freaks me out -- the syntax is really difficult for me to remember and one misplaced curly brace immediately returns a whole slew of error messages. User friendliness rating on a scale of 1 to 10: -3

I was asking one of our TAs, Trevor, for help on my project today and he showed me this great alternative to IRB and Rails console called Pry. Pry-rails is a gem that allows you to run, pause and inspect code that you’re running on your local machine. It’s almost like a time-turner for code.

My favorite part: 2-step installation.

First, add the following gem to your gem file: 
```gem 'pry-rails', :group => :development```

Then:
```bundle install```

And that’s it!

Here’s how to use it: 

1. Put the words ```binding pry``` wherever you think your code may be triggering an error. 
2. Run ```rails server``` in Terminal. 
3. You’ll see that the loader for the web page will start to move slower. Go into Terminal and you’ll see that it now shows something along the lines of ```[1] pry(#<nameofinspectedfile>)>```
4. Type anything that you would normally be able to type into Rails console into Pry to try and figure out why your code is breaking! 
5. Once you’re ready to “un-pause” the code, type ```exit``` and the code should run through to the end again.
