---
layout: post
title: "Everything is an object"
description: "The Ruby object model for classes"
category: Ruby
published: false
tags: [Ruby, metaprogramming]
---

They say everything in Ruby is an object. But what does that mean? How can, for example, a class be an object?

A class defines how an object behaves. It's the template of a certain category of objects. How can a class on it's own be an object? And if it's an object what class does a class have?

Well, let's look at some properties of objects and see if a class has them, too.

1. Objects are created by calling the function 'new' on their class.


       a = String.new("Hello world")
         -> "Hello world"

1. Objects can be assigned to other objects.

       o = a
        -> "Hello world"

1. Objects have a class.

       a.class
         -> String

So how do classes compare to this?

1. Classes can also be created with 'new'.


       Person = Class.new do
         def initialize
         end
       end

1. Classes can be assigned to other objects.

       b = String
       a = b.new("Hello world")
         -> "Hello world"

1. Classes also have a class.

       Person.class
         -> Class
       Person.class.class.class
         -> Class

I hope you aggree, that classes surely behave like objects. But it still feels strange. I hope this class diagram helps.

![Ruby Class Diagram](/assets/ruby_class_diagram.png)
