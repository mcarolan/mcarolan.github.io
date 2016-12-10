---
layout: post
title: flatMappy bird follow up material
comments: true
---

<p>A huge thanks to everybody who attended my talk at <a target="_blank" href="https://skillsmatter.com/conferences/7432-scala-exchange-2016">Scala eXchange 2016</a>, &quot;<a target="_blank" href="https://skillsmatter.com/skillscasts/8980-flatmappy-bird-functional-flappy-bird">flatMappy bird: functional flappy bird</a>&quot;.</p>
<p>The aim of my talk was to give:</p>
* A feeling for how FRP, and Coroutines work
* Pride in functional programming
* A couple of hints about what to look at if it peaked your interest
<p>Here are a few things to point you towards the latter!</p>

Coroutines
----

The flatMappy bird project was based on 2 articles:

* <a target="_blank" href="https://github.com/leonidas/codeblog/blob/master/2012/2012-01-08-streams-coroutines.md">Generalizing streams into Coroutines</a>
* <a target="_blank" href="https://github.com/leonidas/codeblog/blob/master/2012/2012-01-17-declarative-game-logic-afrp.md">Purely Functional, Declarative Game Logic Using Reactive Programming</a>

As you can probably guess, I found these absolutely fascinating - and I highly recommend you check them out!

<p>There is also a <a target="_blank" href="http://www.storm-enroute.com/coroutines/">Scala Coroutines</a> library. I have not tried to build anything with this yet, but the documentation looks great - and it&apos;s fully featured. Definitely worth a look.</p>

<p><a target="_blank" href="http://breakpointradio.net/ep-7-23-nov-2016-its-the-end-of-the-world-as-we-know-it/">Episode 7 of Breakpoint Radio</a> also has some great discussion of Coroutine development in Scala and on the JVM.</p>

Scala.js
----

The place to go is <a target="_blank" href="http://www.lihaoyi.com/hands-on-scala-js/">Li Haoyi&apos;s Hands on Scala.js</a>. Whilst you&apos;re there, check out the rest of his website - it&apos;s a treasure trove.

flatMappy bird itself
----
* The project is <a target="_blank" href="https://github.com/mcarolan/flatmappy-bird">available on github</a>
* Along with the <a target="_blank" href="https://github.com/mcarolan/flatmappy-bird-presentation/raw/master/presentation.pdf">slides from my presentation</a>

A challenge
----

<p>Implement &quot;Hello World&quot; with a Coroutine yourself, to understand the concept:</p>

<blockquote>
  <strong>Problem</strong><br/>
    There is a time varying String value that we can sample. We want to transform it to a time varying Boolean:
    <ul>
      <li>The latest value of the String is "World" AND</li>
      <li>The previous value of the String was "Hello"</li>
    </ul>
</blockquote>

<p>Here&apos;s some code to get you started:</p>

{% highlight scala %}
trait CoRoutine[A, B] {
  def apply(input: A): (B, CoRoutine[A, B])
}

val helloWorld: CoRoutine[String, Boolean] = ???

val (res1, next1) = helloWorld("Hello")
println(res1) // should print false

val (res2, next2) = next1("World")
println(res2) // should print true

val (res3, next3) = next2("Foo")
println(res3) // should print false

{% endhighlight %}
<p>This will be easy if you read <a target="_blank" href="https://github.com/leonidas/codeblog/blob/master/2012/2012-01-08-streams-coroutines.md">Generalizing streams into Coroutines</a>.</p>

<p>Enjoy!</p>
