
# Chaos Engineering for Fun and Profit

So lets say you're developing a new web application, that _Next Big Thing_ that's had everyone on the edges of their seats forever. After all the tireless work you've put in, sleepless nights debugging and refining.. It's finally time to launch your service to your would be clientele. Now comes the hard question...


#### When is your Application ready for Production?

Or more to the point, how can you make certain that your distributed system is resilient enough to survive a frequently fickle internet? Let's be honest, you can never be sure (or too sure). You just don't know what (or more importantly when) something bad will happen. There will _always_ be something that can (and inevitably _will_) go wrong. These can range from self-inflicted outages caused by bad configuration values, buggy server images (AMIs or VHDs) or even events that are outside your control such as DDoS'ing attacks or network failures. No matter how hard you try, you can't build the perfect software (let's be honest, you can't build perfect hardware either...). Unfortunately this also bleeds over to the companies that you tend to rely on (I'm looking at you AWS, I remember the US-EAST-1 outage like it was yesterday).

We live in an imperfect world, that's just how it is... It's time to accept that and focus on things that _are_ in our sphere of control, such as creating quality products that are resilient and reactive to failures. Build software that is able to cope with both expected and unexpected results; gracefully degrade whenever necessary. As I often say __Pray for the best, while  always expecting the worst.__

Okay this sounds sweet right? But how? How can you make sure you’re ready for disaster?

The first thing(s) that we'll need to do is to isolate and identify the problems that may arise in a production-esque environment. Only then will you be able to address systemic weaknesses and make our systems fault-tolerant.

This is where [Chaos Engineering](http://principlesofchaos.org/) comes in.


#### Principles of Chaos Engineering

The concept of Chaos Engineering is that, rather that waiting for things to break in Prod (which will always seems to happen at the worst time), we will proactively inject failures (or chaos) in order to prepare for scenarios that will likely arise when disaster _does_ strike. This tends to go hand in hand with another oft cited thing which is _Disaster Recovery_. [Netflix](https://medium.com/netflix-techblog/the-netflix-simian-army-16e57fbab116), who was a pioneer in this field and as to date the defacto standard defines __Chaos Engineering__ as:


 > Chaos Engineering is the discipline of experimenting on a distributed system
 > in order to build confidence in the system’s capability to withstand turbulent
 > conditions in production.
