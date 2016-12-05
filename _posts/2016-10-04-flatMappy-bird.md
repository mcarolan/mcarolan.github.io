---
layout: post
title: flatMappy bird - flappy bird as a pure function
---

Remember that simple yet addictive game from 2014 where a pixelated bird had to avoid crashing into a plagiarised image of a pipe?

Let&apos;s model it as a pure function.
<!-- more -->

## What, but why would we do that?

OK, this is how it all started.
Earlier this year I moved from London to Brighton [LINK], and suddenly found myself with a lot of dead commuting time on my hands. 3 hours each day to be precise.

When you have a long commute you soon learn the necessity of having a buffet of distractions on your person, at all times. I go through phases of:

<ul>
<li>Working, and leaving work early</li>
<li>Watching TV programmes / films</li>
<li>Watching tech talks</li>
<li>Gaming</li>
<li>Reading</li>
<li>Programming</li>
</ul>

Anyway, the list could go on.

One day I was on the gaming phase. The previous night I&apos;d downloaded BitBlaster XL on Steam [LINK] (no affiliation, promise), and was revelling in the pointless yet compelling addiction it provided.

The next day I was on the programming phase again. I was thinking of something fun to work on, and cast my mind back to BitBlaster [LINk]. I thought it'd be dead easy (and fun) to implement a game using ScalaJS [LINK]. I found [LINK]&apos;s blog, read a couple of his posts and started hacking with his excellent workbench platform [LINK].

 I&apos;d settled on making flappy bird for some reason, but then something happened. I spend a lot of my time working on and thinking about functional programming (I know, get a life) and suddenly I was doing things, in Scala, that were hallmarks of imperative programming: loops and the dirty var word.

 I wondered if anybody was writing games that promoted functional programming principles. I then remembered the internet and stopped wondering: of course somebody had. I found these 2 articles

[LINK]
[LINK]

 which give a great account of how to write Pong [LINK] using the concept of a CoRoutine [LINK]

 <h2>A CoRoutine?</h2>

 That&apos;s what I said. I really encourage you to spend some time with those articles to discover CoRoutine&apos;s in depth - but I am going to give a brief intro right now.

 First, let's take a brief look at CoRoutine's ancestor, `scala.Function1`

 This is dead simple, and vaguely looks like:

 {% highlight scala %}
  trait Function1[A, B] {
    def apply(input: A): B
    ...
  }
 {% endhighlight %}

It a wrapper of a function that takes 1 input, and produces 1 output.

IDEA: draw something that receives a time varying input (e.g. is even second of epoch) 

With a CoRoutine we add another dimension to this.

A `CoRoutine` builds on this a bit by considering computations that receive inputs over time.

{% highlight scala %}
trait CoRoutine[A, B] {
    def apply(input: A): (B, CoRoutine[A, B])
}
{% endhighlight %}

It wraps a function that takes 1 input, and returns 2 outputs.
<ul>
<li>The first output is the result of the computation after </li>
But the second output is special: it is another CoRoutine, and you should use it to compute the next output when the next input is available.


<h2>Pure, you say?</h2>

Yes. More information on what a pure function means, and why you should care is available at [LINK].

But as a jist:

<ol>
<li>The function always evaluates the same result value given the same argument value(s)</li>
<li>Evaluation of the result does not cause any semantically observable side effect or output</li>
</ol>

<h2>How do things move if the game function is pure?</h2>

Let&apos;s have a gander at the encoding in Scala again:

{% highlight scala %}
trait CoRoutine[A, B] {
    def run(input: A): (B, CoRoutine[A, B])
}
{% endhighlight %}

The secret sauce is that the CoRoutine gives you a result, and another CoRoutine you should use to compute the next result.

This allows for previous inputs (or things derived from previous inputs) to be passed to future computations.

Put another way, it models a computation where the historical inputs and currently perceived input affect both the next output, and the future flow.

<h2>The power is in the composition</h2>

As with any functional data structure or pattern, you get the true power when composing them together. The premise is:

<ol>
<li>Define small, easy to reason about (and test) atoms of your description</li>
<li>Compose them together to make something that forms a larger, more complex description</li>
</ol>

Note: I&apos;m purposely using the word description rather than action or effect as I believe a well designed functional program should be
a description of behaviour, not an imperative recipe to follow.

<h2>How does the player in flatMappy bird move?</h2>

Well, the player moves in 2 different ways:

<ul>
<li>Falls at a constant rate, irregardless of input</li>
<li>Rises at a constant rate if the spacebar is held</li>
</ul>
