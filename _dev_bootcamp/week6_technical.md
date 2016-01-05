---
layout: page
title: How to Cope with Variable Scope
---

Variable Scope What kinds of variables does Ruby support? Where are they accessible? When would you use them and what makes them different?

My desire to write about variable scope in Ruby is, truth be told, largely due to the frequency that I initially get it wrong when writing code. And then I have to pause, and think 'Why the hell didn't that work?'. Then I correct the avoidable problem, rebuke myself gently and then move on. If I could forgo these interruptions, I think I will be a more productive, and definitely a happier programmer.

Ruby has four variable definitions, each with a different scope and syntax. Below is a table outlining the basics.

## Local Variables

Local variables start with a lowercase letter or an underscore. They can contain letters, numbers and underscores, but they always start with a lowercase letter or an underscore.

Local variables are limited in scope. They are only accessible within the method or block where they were created. I think of them in terms of writing on the back of a napkin. It is useful for working through a problem, but you don't keep the napkin as a final product. You toss it when you are done. You certainly don't share it with others.

<pre class="prettyprint">  local_variable
  _local_variable
  local_variable_1
  localVariable (**valid, but not used in Ruby by convention)

</pre>

* * *

## Instance Variables

Instance variables always start with a single @ sign.

Instance variables are available to all methods within a particular class. This allows you to structure your code such that discrete methods within your class can change the value of a the same variable.

<pre class="prettyprint">  @instance_variable
  @Instance_Variable
  @InstanceVariable

</pre>

* * *

## Class Variables

Class variables always start with 2 @ signs.

The analogy I use to remember when a Class Variable might be useful is the eventual standardization of the gage of railways in America after the Civil War. Prior to the end of the war, the width of the train tracks in the Northern States was different than in the Southern States. This caused all kinds of problems, for obvious reasons. When a Class Variable's value is changed, that change automatically propagates to all objects created from that class. (It would have been nice to be able to change all of the train cars created from the TrainCar class to use the new track gage by just changing the Class Variable.

<pre class="prettyprint">  @@class_variable
  @@Class_Variable
  @@ClassVariable

</pre>

* * *

## Global Variables

Global variables always start with a single $ sign. They are accessible anywhere within your application. I think of Global Variables in the same way as I think of tattoos. They are kind of a big deal and should be used with caution. I am very reluctant to use them, primarily because I can't really think of any application that makes sense for them.

That being said, there are several pre-defined Global variables that are useful for debugging and gathering information about your application. A table listing them is available at [http://www.techotopia.com/index.php/Ruby_Variable_Scope#Ruby_Global_Variables](http://www.techotopia.com/index.php/Ruby_Variable_Scope#Ruby_Global_Variables)

<pre class="prettyprint">  $global_variable
  $Global_Variable
  $GLOBAL_VARIABLE

</pre>