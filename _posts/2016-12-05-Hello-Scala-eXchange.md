---
layout: post
title: Hello, Scala eXchange!
---

<p>This Thursday I&apos;m hitting a foreboding but exhilarating milestone: giving my first talk at a conference.</p>
<p>I&apos;ve got the pleasure of delivering a lightning talk entitled "flatMappy bird: functional flappy bird" at <a href="https://skillsmatter.com/conferences/7432-scala-exchange-2016">Scala eXchange 2016</a>.</p>
<p>In this post I wanted to share my experience (so far!) of being a first time speaker, and help spread some tips and encouragement for anybody interested in setting themselves a 2017 challenge!</p>

How did it all start?
----

<p>Well, I&apos;d had an itching to do something like this for a while. It turns out an itching doesn&apos;t cut it when faced with the unboundless procrastination potential gifted by a <a href="https://en.wikipedia.org/wiki/Academic_conference#Organizing_an_academic_conference">CFP email</a>.</p>
<p>Like most things I&apos;ve done in life, a healthy dose of peer pressure was required to get me started. This came in the form of badgering from <a href="http://www.sofiacole.com/">Sofia Cole</a>. I&apos;m very grateful for this, and would almost certainly not have followed through with it otherwise !</p>

```
Tip 1: find someone willing to badger
```

Why did you decide to do a lightning talk?
----

<p>For me, the amount of anxiety this was beginning to induce (even before the <a href="https://en.wikipedia.org/wiki/Academic_conference#Organizing_an_academic_conference">CFP stage</a>) meant I was mentally refusing to do anything more than a lightning talk. So that was cool: identifying constraints is a good thing.</p>
```
Tip 2: work out your mental constraints (are you confident enough to dive into a full length talk?)
```

How did you decide on the subject?
----

<p>I had a bit of a Google for how to give engaging lightning talks, and that made me consider 2 candidate projects I was working on at the time:</p>

<ul>
<li>A Scala AMQP library, that gives a nice wrapper around the <a href="https://github.com/rabbitmq/rabbitmq-java-client">RabbitMQ Java AMQP library</a>  </li>
<ul>
  <li>This is now in production use at <a href="http://www.itv.com">ITV</a>, we hope to open source it very soon (but I&apos;ve been saying that for a while!)</li>
</ul>
<li>This weird flappy bird game I was hacking together on my commute, that partially worked</li>
</ul>

<p>I quickly wrote off the first idea. It&apos;s a great project, but I felt it&apos;d be hard to hold the interest of viewers who were not currently using AMQP based messaging (which I&apos;d figured would be a fairly significant portion).</p>  

<p>I found the flappy bird game I was hacking together on my commute absolutely fascinating.<br/> To be honest, I hadn&apos;t taken time to understand how some of the more abstract parts of it actually worked! I&apos;d kind of lost motivation in this project as soon as I had cracked the interesting part: getting the player moving based on time and key presses using a <a href="https://github.com/leonidas/codeblog/blob/master/2012/2012-01-08-streams-coroutines.md">CoRoutine</a>.</p>

<p>So that was it: I opted to pick something I was dead interested in, but hadn&apos;t yet invested a lot of time in. If it got selected I&apos;d be forced to revisit my hacky side project in depth and distill it into a 15 minute talk.</p>

<p>I thought up of a click-baity title, and left it to Future Martin to deal with any consequences.</p>

```
Step 3: decide what you think is important in a talk: and see if anything you're working on fits (even if it isn't fully finished!)
```

So then you just waited for the yes/no email?
----

<p>Nope. In my head I was fairly sure my submission wouldn&apos;t amount to anything. But again, the amount of anxiety I was experiencing with this was through the roof! "What if it did get accepted?! I&apos;d be screwed - I&apos;m not confident with the project yet!"</p>
<p>I decided to scrap my original hacky implementation of the game, and remake the project with a view to fully understanding how even the most intricate pieces of it worked. Just in case.</p>
<p>I figured it&apos;d be good to do anyway: I did find the subject incredibly interesting. And it wouldn&apos;t be wasted: I could always translate it into a Meetup talk or a blog post.</p>

```
Step 4: mild post submission panic
```

Flash forward a couple of months
----

<p>Woke up, checked my emails: "Scala eXchange 2016 - Your submission has been acccepted!".</p>

<p>Oh, crap!</p>

<p>I always find it intruiging how something like an email can have such a big impact. At this moment it was a pure rush, and I was over the moon with the opportunity.</p>

```
Step 5: submission accepted email elation!
```

Did you accept immediately?
----
<p>Pfft, nope. There are several stages of committment in my mind. The adrenaline rush is but the first.</p> 
<p>It was irrational, but I was extremely anxious that even though I now had a decent implementation (which would form the basis of my talk) - I had no actual talk. So cue the procrastination.</p>
<p>Eventually, reason came into play. I had a solid base, and months to turn it into a talk I wanted to deliver. I accepted. Future Martin can deal with it.</p>

```
Step 6: submission accepted email panic!
``` 

Building the talk
----

<p>Now, this point was probably rock bottom for me. Future Martin did indeed have to deal with it.</p>

```
I've got a decent base for a talk now. But there's so much I want to cover, and I only have 15 minutes. I think I've shot myself in the foot by constraining it to a lightning talk. It's going to end up having no substance!
```
Martin Carolan, 2016

<p>I did the opposite of the stellar advice later given to me in Jenny Martin&apos;s brilliant <a href="https://skillsmatter.com/courses/550-how-to-give-technical-talks#programme">"Giving Engaging Talks at Conferences and Meetups"</a> training course, and:</p>

* Had no structure or story
* Dived straight into making slides (with lots of bullet points!)
* Drew random (complicated!) diagrams with no hope of explanation within 15 minutes
* Made some code samples and challenges that were great for describing the intricacies, but were not feasible (or fun) to grok within 15 minutes

<p>For me, the way I got into a more confident mindset was by having a panic and then:</p>

* Accepting that within 15 minutes you&apos;re probably not going to be able to:
  *  deliver a groundbreaking talk that fundamentally challenges the audience
  *  delve deeply into how a  non-trivial data structure or algorithm the audience are not familiar with works, along with applications and critical analysis
* And realising that, within 15 minutes you _CAN_ instead:
  * tell a story that engages the audience 
  * introduce the background of a potentially new concept and explain (at a high level) how it works
  * show an interesting application of it
  * give materials to further their knowledge, if they are interested 

<p>From this, the anxiety did start to dissipate. I started to feel that I hadn&apos;t shot myself in the foot, and it could all be worthwhile.</p>

```
step 7: remember what you think the audience will want from your talk, plan and build around that
```

Practising the talk
----

<p>People will give majorly conflicting advice about whether to(!) and how much to practise.</p>

<p>I think it&apos;s a pretty personal thing, but for me I had to practise over and over to get to some normal level of confidence. I&apos;m still expecting to be nervous and doubting on Thursday, but right now I feel prepared and that it&apos;s something I can get through.</p>

<p>
My advice is to run through as much as you can, with people from as many diverse backgrounds as you can muster.
</p>

<p>
If you can, get yourself a slot at a local Meetup a couple of weeks before your actual conference talk. <br/><a href="https://www.meetup.com/Scala-Central/">Scala Central</a> were kind enough to let me speak. It forced me to have everything prepared, gave me experience of speaking to a decent sized audience, and gave me some feedback to implement before the real deal.<br/>This helped my anxiety to to reduce together near-zero.</p>

<p>
In terms of resources to help you be more confident in delivery:

<ul>
<li><a href="https://skillsmatter.com">Skills Matter</a> were kind enough to send Scala Exchange speakers on Jenny Martin&apos;s excellent <a href="https://skillsmatter.com/courses/550-how-to-give-technical-talks#programme">"Giving Engaging Talks at Conferences and Meetups"</a> course</li>
<ul>
<li>I thourourghly enjoyed this, it enabled lots of opportunity to practise delivery in a safe environment - and gave some focus on the areas I personally need to concentrate on</li>
</ul>
<li>There are lots of meta talks-on-giving-talks out there. One I particularly enjoyed was <a href="https://www.youtube.com/watch?v=l9JXH7JPjR4">Ben Orenstein&apos;s "How to Talk to Developers"</a></li>
<ul>
<li>Probably worth finding a few for yourself - people want to aim for different things from their talks.</li>
</ul>
</ul>
</p>

```
step 8: keep on practising!
```

Actually doing it
----

<p>Well, I haven&apos;t actually done this yet. So who knows how it&apos;ll go and how well it&apos;ll be received!</p>

<p>I know for sure that I&apos;ll be dead nervous on Thursday. But I also know that if I practise any more it&apos;ll sound over-rehearsed, and speaking at <a href="https://www.meetup.com/Scala-Central/">Scala Central</a> a couple of weeks went better than I expected it to.</p>

```
step 9: who knows!
```
