---
layout: page
title: A few good shortcuts
---

Here are a few good shortcuts I have learned for Ruby

* * *

## Arrays

Arrays are great for storing secquenced data.

<pre class="prettyprint">  array = [1, 2, 3]
  array_strings = ["First", "Second", "Third"]
  array_shortcut = %w[First, Second, Third]
  #To call an element in an array
  array_shortcut[2]
</pre>

## Hashes

Hashes handle key-value paring really well.

<pre class="prettyprint">  hash = {"first" => "first_value", "second" => "second_value"}
  hash_symbols = {first: "first_value", second: "second_value"}
  #To call an element in a hash
  hash_symbols[:first]
</pre>

## Evaluations

If it is answers you seek, ask the right questions.

The venerable if else

<pre class="prettyprint">  variable = "yes"
  if variable == "yes"
    puts "this is true"
  elsif variable == "no"
    puts "This is false"
  else
    puts "Maybe?"
  end
</pre>

A prettier form

<pre class="prettyprint">  puts "This is an if" if true
</pre>

Unless is a nice twist

<pre class="prettyprint">  puts "This is an unless" unless false
</pre>

This is taking a ternary for the worst

<pre class="prettyprint">  puts 1 > 0 ? "This is true" : "This is false"
</pre>

Whatever the CASE may be

<pre class="prettyprint">  puts "Hello there!"
  greeting = gets.chomp

  # Add your case statement below!
  case greeting
    when "English" then puts "Hello!"
    when "French" then puts "Bonjour!"
    when "German" then puts "Guten Tag!"
    when "Finnish" then puts "Haloo!"
    else puts "I don't know that language"
  end
</pre>

This nifty short cut assigns a value unless one already exists.

<pre class="prettyprint">  favorite_language ||= "Ruby"
</pre>