Reactive Programming Exercise With baconjs
=====================
The goal of this exercise it to practice and learn about the concept of reactive programming. We successfully ran this exercise at the Boston Software Craftsmanship Group with 8 people. It could scale well to a group of about 18. From start to end it took about 2+ hours to run.

This exercise uses baconjs for it's reactive programming framework. Javascript was a good choice for the language because there's zero overhead in getting an environment setup, and baconjs turned out to be a good choice as well because it is fairly well documented with fairly simple concepts. 

The Event
---------
* 15 minute discussion about reactive programming. Make sure people understand the basic concepts and reasoning for reactive programming. I started the discussion by asking the group to explain reactive programming. This turned out well because: (a) I'm no expert (b) I suspected, and was correct that a number of people were familiar with the concept (c) It seemed like a good way to foster dialog.
* 15-30 minutes Introduce the kata, review baconjs, review the bootstrap code. When we ran this exercise it was helpful to whiteboard different concepts. At this point in the exercise, it's critical that most people in the group understand the basic concepts. You don't want groups breaking off into teams if they are missing core concepts.
* Break groups off into teams of ideally 3 people. With two people, you run a higher risk of not having a team that groks the assignment. With four people, you run a higher risk of having people feeling left out. The goal is active participation from everyone. If you can spread out your stronger developers across the teams, this is not an exercise where you want teams to struggle.
* Encourage people to plan their design on pen and paper first. Streams lead to visual references really well, and it can be easier to come up with a plan first rather than trying to design on the fly.
* Have everyone pause after an hour or so and do a check in. Have each group say a thing or two about their approach and what they learned so far.
* Save 20 minutes at the end and have each group present what they did and what they learned!

DOCS
---
Some docs to help you get going:   
https://github.com/baconjs/bacon.js     
http://www.cheatography.com/proloser/cheat-sheets/bacon-js/   
https://github.com/baconjs/bacon.js/wiki/Diagrams   
http://nullzzz.blogspot.fi/2012/11/baconjs-tutorial-part-ii-get-started.html  


THE KATA
--------
This kata simulates a simple email system. A user will type in one or more email messages into the "To" input field and a message in the "Message" input field. Now this isn't just some boring old email system. No, this system is for the geek who likes to see what's sent over the wire. So your job is to display a simplistic SMTP message as the geek is typing, cause well that's just the kind of person they are. Not only does this geek want to see the SMTP they also want to see any mistakes in realtime as their typing. You forget an @ symbol in an address, show that error. 

STEPS
------
**One address, simple message:**  
to: joe@example.com  
message: Hi how's it going?
SEND Button is enabled
Network area shows:  
"connect smtp  
To: joe@example.com  
    
Hi how's it going?  
  
disconnect  
"    

**Addresses need an '@' sign.**  
to: joenoatexample.com  
message: Hi how's it going?  
The incorrect address should be shown in the errors section.  With a note: Needs '@' sign  
The SEND Button is disabled.  
Network area shows:
"connect smtp  
To: joenoatexample.com  
    
Hi how's it going?  
  
disconnect  
"    

**Send to multiple addressess**  
to: sally@example.com joe@example.com  
message: Hi All.  
SEND Button is enabled
Network area shows:  
"connect smtp  
To: sally@example.com  
To: joe@example.com  
    
Hi All.  
  
disconnect  
"    

