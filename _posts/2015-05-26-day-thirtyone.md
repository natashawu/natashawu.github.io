---
layout: post
title:  "Day #31 - Intro to Rails"
---
Prior to this course, I was telling anyone who asked that I would be learning Ruby on Rails, not knowing at all what Ruby or Rails really was. A typical conversation went like this: 

“Oh, cool! Do you know what languages you’ll be learning at the bootcamp?”

“Yeah, we’ll be starting off with Ruby and going on to Ruby on Rails.”

“Nice!”

*both smiling, nodding and equally confused*

Thankfully, today changed all that. Historically: 

* Rails was created as an open source project in 2004 by, co-founder of Basecamp and supposed programming badass, David Heinemeier Hansson (from this point forward referred to as DHH). I don’t know much about DHH, but he’s pretty famous in the coding world. And according to his Wikipedia page, he also drives race cars! I’d say that’s pretty badass.

* Rails is basically a giant Ruby gem (but most people call it a framework) where a lot of people wrote a lot of code to make it easier to get a website up and running quickly.

Rails follows a model called MVC, which stands for “model-view-controller.” This is the convention that Rails uses to organize where code goes in a web application.* In very simplified terms, a controller tells a model what to do. A model grabs the appropriate data from the database (based on what the controller tells it to get) and passes it to the view. A view generates an output for the user to see based on the data that the model passes to it. Of course, there’s a little more back and forth and it’s not always a perfect loop, but that’s how I like to think of it in a general sense. 

In our class, we like to think of the flow as being RCV -- “routes-controller-view.” In the routes file, you list all the possible web request combinations for your site. That means that if you want to have: thingsilove.com/cookies/index, thingsilove.com/cookies/about and thingsilove.com/cookies/new, you would have to list this in the routes file in the following fashion:

```get “/index” => 'cookies#index’```

Where ```get``` is the verb, ```/index``` is the url, ```cookies``` is the controller and ```index``` is the name of the controller action. Remember, a [web request]({% post_url 2015-05-25-day-thirty %}) is an HTTP verb + a URL. 

At first, all these rules and conventions seemed kind of daunting, but I quickly realized how much of a pain it would be to make a website without them. Everything would be a mess of a billion files -- with random names, in random folders. In that situation, I don’t even want to think about trying to pick up something another developer has already started. So thank you, Rails (and I guess DHH + co.) for making life easier. 

* Wait, “web application?” Don’t you mean “web site?” Or “mobile application?” No, I mean “web application.” And yes, it is confusing. I like to think that most modern websites are web applications -- they require user interaction to be useful. Web applications allow users to do anything from comment on a post to look up a destination on an interactive map. Web sites, on the other hand, are static pieces of the Internet that display information for the user to consume -- think of your local bar or grocery store’s online website. You can’t comment on anything or shop online, the only thing you can do is read about today’s specials and find out what their store hours are. For further explanation, look [here](http://www.visionmobile.com/blog/2013/07/web-sites-vs-web-apps-what-the-experts-think/ "Web sites vs. Web Apps").