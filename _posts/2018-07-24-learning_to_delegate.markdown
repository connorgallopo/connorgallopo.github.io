---
layout: post
title:      "Learning to Delegate"
date:       2018-07-24 15:10:29 +0000
permalink:  learning_to_delegate
---


Throughout my Rails project I found myself in a pretty repetitive workflow when implementing class methods. I would have a working view, start to implement new functionality and soon find out that it breaks when accounting for nil. This is when I first discovered the Safe Navigation Operator in Ruby. Basically what this does is return nil if a method is called on a nil object instead of throwing a NoMethodError. This proved to be immensely useful but i found that i was implementing them everywhere and I knew there had to be a better way.

This is when I leared about delegate in Rails. This is a very handy way of creating a certain behavior but delegate the responsibilty for implementing it to another method or associated object. It's especially easy when there is an activerecord association.

To better explain i'm going to use the example below. Lets say we have a User class and a Ticket class. The ticket belongs to the user and the user has many tickets. An attribute of the user would be email. So if I wanted to write a quick class method to display the email of the tickets user it would look like this:
```
def user_email
  self.user&.email
end
```

In this scenario I decided to use the Safe Navigation Operator becuase at this point I cant be sure that every user will have an email. But there is actually a much better way to write this with the same functionality using delegate. See below:

```
delegate :email, to: :user, allow_nil: true, prefix: true
```

So this is doing a couple things. `:email` is the method name, `to: :user` is the object that we will be calling that method on. So this is the same thing as the method `user_email` written above. Where it gets interesting are the two options that were also used. `allow_nil` is taking the place of the Navigation operator and preventing the NoMethodError, and `prefix:true` is helping name the method. When prefix is added you will call the method by putting the object name before the method name and seperating the two with and underscore. So when I want to call this method in my application I would use `@ticket.user_email` and this would be a much cleaner and more performant version of my original method.

