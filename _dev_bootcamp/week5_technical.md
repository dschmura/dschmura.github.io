---
layout: page
title: What does the Fox say?
---

## Keeping it Classy

When I was a kid, I grew up near a restaurant in Bloomfield Hills, Michigan called [Machus Red Fox](http://www.whatwasthere.com/browse.aspx#!/ll/42.542586,-83.285135/id/42110/info/details/zoom/14/) (you may have heard about it as the last place where Jimmy Hoffa was seen before his disappearance in 1975). I remember the restaurant as a classy place, so much so in fact that I took my homecoming date there my Freshman year of high school.

Foxes are known, historically to be wily, clever creatures. They are cunning and conniving...all which go to say...they are intelligent beasts. This morning I was thinking about blogging about classes and couldn't stop thinking about the fox. And then it happened...that song...you know the one...got stuck in my head. Since I am immersed in thinking in code, I immediately thought of the driver code I would use to answer the question: What does the fox say?

<pre class="prettyprint">  fox.what_do_you_Say?
</pre>

Before we answer that though, let me circle back to what a Class is in Ruby.

## Ruby Classes - A defining achievement

The underlying idea behind Classes is to abstract patterns into reproducible definitions. Classes are a special kind of construct that allows you define a template for creating objects. A Class comprises what an object is, and what it can do. That is, Classes define what data (state) an object holds and the methods (things that the object can do) of the objects that get created with it.

One of my favorite things about the Ruby language is that everything is an object. Even Classes are objects that are of the Class Class. It really is a very cool idea. So, when you create a new Class, you are automatically inheriting the functionality of the Class Class.

So, to answer our question, we need a way to create a fox that we can ask. Creating a 'Fox' Class seems a little specific (but that is a design decision), so I am going to create a 'Canine' Class. The Canine Class is concerned with two things (for the purposes of this example anyway); 'type' (is this a dog, a fox, a wolf etc...) and 'bark' ("Woof", "Bow Wow", "Howl" or the like ).

'type' and 'bark' are arguments that we will pass to our Canine Class. For this explainer, that is the minimum that we need to solve the problem. When we pass these arguments to our Class, we kind of hope that something happens. Since computers are kind of dumb, we have to tell them what to do. So, to kick things off, we tell the Class to initialize.

I think of the initialize method as the Inn Keeper. It is responsible for creating your object's initial state. You can pass the initialize method arguments (if you set it up that way) and it will use these arguments to set the value of variables in your object. The values may change during the lifetime of the object.

<pre class="prettyprint">  class Canine
    def initialize(type, bark)
      @type = type
      @bark = bark
    end
  end

</pre>

At this point we could create our new object, but it would be fairly unimpressive because it wouldn't do anything. While that is true of my canine while I am at work, I think we want our canine to be able to respond when we send it a message. To do this, we add a method to our class. Since we are interested in what the fox says, let's add a method that returns the answer to the question. We will create our 'what_do_you_say?' method, which will return @bark (which is the variable holding the argument we passed when we created the object in the first place).

<pre class="prettyprint">  class Canine
    def initialize(type, bark)
      @type = type
      @bark = bark
    end

    def what_do_you_say?
      @bark
    end
  end

</pre>

And, just for fun, let's add another method that let's our Canine run.

<pre class="prettyprint">  class Canine
    def initialize(type, bark)
      @type = type
      @bark = bark
    end

    def what_do_you_say?
      @bark
    end

    def run
      "Tiny paws, up the hill, suddenly you're standing still."
    end
  end

</pre>

Now that we have our new object maker (our new Class), let's use to create a new object. To carry the metaphor further we will create a fox named 'guy_fox'. Since my Canine Class requires two arguments to initialize, we will pass in the 'type' of Canine as "fox" and the 'bark' as "Bay-buh-day bum-bum bay-dum" (which is, it turns out, what the fox actually says. For proof please see [this incontrovertible video evidence](https://www.youtube.com/watch?v=jofNR_WkoCE) !

<pre class="prettyprint">  guy_fox = Canine.new("fox", "Bay-buh-day bum-bum bay-dum")
</pre>

Now that we have created our fox, we can send it messages and it can do stuff. So for example we can say;

<pre class="prettyprint">  guy_fox.run
</pre>

Or

<pre class="prettyprint">  guy_fox.what_do_you_say?
</pre>

and we can get a response. Our object actually knows what to do...because we told it!

When creating a class it is important to think in terms of what absolutely has to been there? What I mean is, what are the aspects of the thing that we are defining in the class? If a particular thing does not define what makes the thing _the thing_ then it probably should not be included in the Class definition. It can be added to an instance of the Class if there is a reason, and Classes can be extended, but it is important to avoid muddling Classes with things that don't belong.

Classes provide a way to define a framework for creating objects that share the same types of information and behavior.