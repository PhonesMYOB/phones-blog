---
layout: post
author: pedro_coelho_pais
title:  "Learning how to learn, JavaScript, I can't read"
date:   2018-02-15 10:38:35 +1100
categories: jekyll update
---
Last week was quite something. I'm still ajusting with writing my blog and keeping up with everything I've learnt, so I probably missed
and/or forgot some things, so if I remember them later I'll update this/create a new post. Today I'll list what I've learnt into points
rather than a big rant like last post because I feel I've went through a lot. So here they are:

Lesson number 1: Learning how to learn
I guess it's good to learn this early on, but really I should have known this. Last week on the first few days I tried to do a lot of
things at once, and just like when we had to build a spaghetti tower to hold a marshmellow, it came crumbling down. I felt like
I got a few things but didn't feel like I learnt that much. It wasn't a great feeling. But from that, I understood that if I just focused
on one area of learning for a period of time, I would absorb a lot more knowledge. I also learn a lot more from seeing examples and trying to
reproduce them rather than just reading about things. 

Lesson number 2: Learning how to TDD+pair program (Again) with the great Mark Pearl
Again, reiterating on the knowledge we had with Matthew and Preethi, except this time we already knew how to do certain things, e
xcept that one time I paired with Tony and we spent the whole time trying to set up jUnit, that one was a painful but 
valuable lesson that you can't name your Test class 'Test'. This whole experience was super useful to see how everyone has specific gaps
of knowledge and that no matter how much you think you are not as good as other people, you can still know certain things that they
don't because no one has the exact same experience. I also learnt a lot of keyboard shortcuts, and had the opporunity to witness
a small window of what it's like to use VIM to navigate around. Looking at Mark doing all this cool stuff on the computer really
inspires you to learn that, so I'll probably try to start that next week.

Lesson number 3: Learning how to organise a project
I had a talk with my mentor Kenneth, and we went over how to truly break down a project (Or he also called them 'Epics'). Remember to know what you know
and know what you don't know but focus on the former.


Lesson number 4: Learning some JavaScript (the hard way)
I was browsing for my daily kata on codewars, and I found one for MTG (Magic The Gathering), and being the naive foolish boy I was
back then (Read: 3 days ago) I thought "This should only take 2 hours". It took me the whole day. Granted, I had other things happening
during the day, but that was all the coding I did that day. 

<ul>
<li>JavaScript strings are not objects so you cant just pass a string variable on a method and expect it to be mutated</li>
<li>To add an x number of chars to a string, you have to create an array of size x and fill it with the char you want, and then use array.join to create a string</li>
<li>How to use a Map array</li>
<li>Sometimes, completly erasing the function that's giving you a hard time is actually the most useful thing you can do (Thanks Mattias)</li>
<li>Regexing /\d/ will only return the first digit of a number, so it won't return 20 it'll return 2. Use /\d+/ for that.</li>
</ul>

Lesson number 5: Learning that MGMT's latest album is really good
Not IT related I know but you should check it out regardless. Also Frank Ocean's new track is great too.

Lesson number 6: Learning some React
This is also a work-in-progress, but I'm following the tutorials on CodeSchool while I have access to it. They're pretty basic
so far but I think they're helpful. So far it just explains that React uses states (haven't gotten to that just yet) and props (which seem 
to be like arguments but for React components) to update information on the website in real time. All the HTML used are written on JavaScript files
 that are interpreted as JSX (JavaScript XML), basically you write a bunch of HTML on the Render() function of one of your props, and you can do some cool stuff with it.
 
 eg.
 
 class MyClass extends React.Component{
  render(){ 
    return(
      //Put your html here
    );
  } 
 }
 
 
Also, if you want to do string interpolation in react, make sure you turn it into a javascript object for whatever reason, which means
embrace it the curly braces.

eg.
An img src would look like this (Using the ES5 and 6 syntax)
src={`{this.props.name}'s my name`}

It seems that anything that's JavaScript related needs to be put inside the curly brackets to be interpreted correctly.
