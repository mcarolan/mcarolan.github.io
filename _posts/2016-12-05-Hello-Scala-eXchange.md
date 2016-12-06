---
layout: post
title: Hello, Scala eXchange!
comments: true
---

<p>In 2 days I&apos;m hitting an intimidating but exhilarating goal: giving my first talk at a conference.</p>
<p>I&apos;ve got the opportunity to deliver a lightning talk entitled "flatMappy bird: functional flappy bird" at <a target="_blank" href="https://skillsmatter.com/conferences/7432-scala-exchange-2016">Scala eXchange 2016</a>.</p>
<p>In this post I wanted to share my experience (so far!) of being a first time speaker, and share some tips and encouragement for anybody interested in setting themselves a 2017 challenge!</p>
<p>Hopefully you&apos;ll see that I realised speaking is entirely subjective, and just like software it is possible to approach it in an iterative manner to gain confidence. The fact I&apos;m able to write this post before my talk  hopefully demonstrates this!</p>

How did it all start?
----

<p>Well, I&apos;d had an itching to do something like this for a while. It turns out an itching doesn&apos;t cut it when faced with the unboundless procrastination potential gifted by a <a target="_blank" target="_blank" href="https://en.wikipedia.org/wiki/Academic_conference#Organizing_an_academic_conference">CFP email</a>.</p>
<p>Like most things I&apos;ve done in life, a healthy dose of peer pressure was required to get me started. This came in the form of badgering from <a target="_blank" href="http://www.sofiacole.com/">Sofia Cole</a>. I&apos;m very grateful for this, and would almost certainly not have followed through with it otherwise!</p>

<blockquote>
<strong>Tip 1</strong>: Find someone willing to badger.
</blockquote>

Why did you decide to do a lightning talk?
----

<p>For me, the amount of anxiety this was beginning to induce (even before the <a target="_blank" href="https://en.wikipedia.org/wiki/Academic_conference#Organizing_an_academic_conference">CFP stage</a>) meant I was mentally refusing to do anything more than a lightning talk. So that was cool: identifying constraints is a good thing.</p>

<blockquote>
<strong>Tip 2</strong>: Work out your mental constraints ASAP (are you confident enough to dive into a full length talk?).
</blockquote>

How did you decide on the subject?
----

<p>I was working on a hacky side project on my commute to work - a flappy bird game.</p>

<p>I found it absolutely fascinating.</p>
<p>But, to be honest, I hadn&apos;t taken time to understand how some of the more abstract parts of it actually worked.<br/>I&apos;d kind of lost motivation as I had cracked the interesting part: getting the player moving based on time and key presses using a <a target="_blank" href="https://github.com/leonidas/codeblog/blob/master/2012/2012-01-08-streams-coroutines.md">CoRoutine</a>.</p>

<p>So that was it. I opted to pick something I was dead interested in, but hadn&apos;t yet invested a lot of time in. If it got selected I&apos;d be forced to revisit my hacky side project in depth to distill it into a 15 minute talk.</p>

<p>I came up with a click-baity title, and left it to Future Martin to deal with any consequences.</p>

<blockquote>
<strong>Tip 3</strong>: Think of something that interests you greatly - that gets some fire in your belly. It's not an issue if you're not fully confident with the subject area yet.
</blockquote>

So then you just waited for the yes/no email?
----

<p>Nope. In my head I was fairly sure my submission wouldn&apos;t amount to anything. But the anxiety I was experiencing at this point was through the roof! <i>"What if it did get accepted?! I&apos;d be screwed - I&apos;m not even confident with the subject area yet!"</i></p>
<p>I scrapped my original hacky implementation of the game, and remade the project with a view to fully understanding how even the most intricate pieces of it worked. Just in case.</p>
<p>I figured it&apos;d be good to do anyway, I did find the subject incredibly interesting. And it wouldn&apos;t be wasted, I could always translate it into a Meetup talk or a blog post.</p>

<blockquote>
<strong>Tip 4</strong>: Use the anxiety/adrenaline (delete as appropriate) of submission, and the lull time to firm up your understanding of the subject area. Your interest in it and the pseudo-commitment can mentally drive you to explore it further.
</blockquote>

Flash forward a couple of months
----

<p>Woke up, checked my emails: <i>"Scala eXchange 2016 - Your submission has been acccepted!"</i>.</p>

<p>Oh, crap!</p>

<p>At this moment it was a pure rush, and I was over the moon with the opportunity.</p>

Did you accept immediately?
----
<p>Pfft, nope. There are several stages of commitment in my mind. The adrenaline rush is but the first.</p> 
<p>It was irrational, but I was extremely anxious that even though I now had a decent implementation (which would form the basis of my talk), I had no actual talk. So cue the doubtful procrastination.</p>
<p>Eventually, reason came into play. I had a solid base, and months to turn it into a talk I wanted to deliver. I accepted. Future Martin can deal with it.</p>

<blockquote>
<strong>Tip 5</strong>: With a base project and weeks (if not months) of potential refinement you will be able to deliver something you're happy with. Go for it!
</blockquote>

3 weeks before the talk
----

<p>Now, this point was probably rock bottom for me. Future Martin did indeed have to deal with it!</p>

<i>&quot;I&apos;ve got a project to base a talk on, but there&apos;s so much I want to cover - I&apos;ve got loads of sample code, diagrams and ideas for interactive demos. But my slot is only 15 minutes. I think I&apos;ve shot myself in the foot by constraining it to a lightning talk. It&apos;s going to end up having no substance!&quot;</i>
Martin Carolan, 2016

<p>For me, the way I turned this into a more productive mindset was by having a panic and then:</p>

* Accepting that on your first ever speaker gig, with a 15 minute slot, you&apos;re probably not going to be able to -
  *  deliver a groundbreaking talk that fundamentally challenges the audience
  *  delve deeply into the intricacies of how a  non-trivial data structure or algorithm the audience are not familiar with works, along with applications and critical analysis
* And then realising that you _CAN_ however -
  * tell a story that engages the audience 
  * introduce the background of a potentially new concept and explain (at a high level) how it works
  * demo an interesting application of it
  * mention materials to further their exploration into the area, if they are interested

From this, the anxiety did start to dissipate. I started to feel that I hadn&apos;t shot myself in the foot - just the toe. And it could all be worthwhile!

<blockquote>
<strong>Tip 6</strong>: Be comfortable with the audience's expectations of your first 15 minute lightning talk. It need not be earth shattering.
</blockquote>

Building the talk
----

<p>I did the opposite of the stellar advice later given to me in Jenny Martin&apos;s brilliant <a target="_blank" href="https://skillsmatter.com/courses/550-how-to-give-technical-talks#programme">"Giving Engaging Talks at Conferences and Meetups"</a> training course, and:</p>

* Had no structure or story
* Dived straight into making slides (with lots of bullet points, sample code, and complicated diagrams!)

My way out of this was to scrap the slides and instead write a narrative (kind of like this!). I never published this, it was just a way to have a soliloquy that could later be recalled and supported by a few images and focus words. Your mileage my vary.

<blockquote>
<strong>Tip 7</strong>: Don't dive straight into slides. I found it useful to write down a story, and later add supporting materials where appropriate.  
</blockquote>

Practising the talk
----

<p>People will give majorly conflicting advice about whether to(!) and how much to practise.</p>

<p>I think it&apos;s a pretty personal thing, but for me I had to practise over and over to gain some normal level of confidence.</p>

<p>
My advice is to run through as much as you can, with people from as many diverse backgrounds as you can muster.
</p>

<p>
If you can, get yourself a slot at a local Meetup a couple of weeks before your actual conference talk. <br/><a target="_blank" href="https://www.meetup.com/Scala-Central/">Scala Central</a> were kind enough to let me speak. It forced me to have everything prepared, gave me experience of speaking to a decent sized audience, and gave me some feedback to implement before the real deal.<br/>This helped reduce my anxiety tenfold.</p>

<p>
In terms of resources to help you be more confident in delivery:

<ul>
<li><a target="_blank" href="https://skillsmatter.com">Skills Matter</a> were kind enough to send Scala eXchange speakers on Jenny Martin&apos;s excellent <a target="_blank" href="https://skillsmatter.com/courses/550-how-to-give-technical-talks#programme">"Giving Engaging Talks at Conferences and Meetups"</a> course</li>
<ul>
<li>I thoroughly enjoyed this, it enabled lots of opportunity to practise delivery in a safe environment, and gave some focus on the areas I personally needed to concentrate on</li>
</ul>
<li>There are lots of meta talks-on-giving-talks out there. One I particularly enjoyed was <a target="_blank" href="https://www.youtube.com/watch?v=l9JXH7JPjR4">Ben Orenstein&apos;s "How to Talk to Developers"</a></li>
</ul>
</p>

<blockquote>
<strong>Tip 8</strong>: Keep on practising! Speak at a smaller gig a couple of weeks before the conference.
</blockquote>

Actually doing it
----

<p>Well, I haven&apos;t actually done this part yet. So who knows how it&apos;ll go, and how well it&apos;ll be received.</p>

<p>I know for sure that I&apos;ll be dead nervous on the day. But I also know I had those nerves for days before my practise run at <a target="_blank" href="https://www.meetup.com/Scala-Central/">Scala Central</a> - and I&apos;m still here to tell the tale!</p>

<p>I have areas I need to develop as a speaker, and this presentation will never be a keynote - but cheers to iteration!</p>


