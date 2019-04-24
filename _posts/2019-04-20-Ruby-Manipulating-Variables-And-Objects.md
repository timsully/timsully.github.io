---
layout: post
title: How Ruby Manipulates Variables and Objects and Passes Them Around
---

- Re-assignment doesn't change the object, it binds a new object to the variable
- Re-assignment to a variable doesn't change the object referenced by that value
- Re-assignment isn't considered a destructive operation
In Ruby, numbers & boolean values are immutable
- nil(the only member of the NilClass class) and Range objects(1..10) are immutable
- Regardless of which strategy a language employs for a given argument or method, it's important to know which one is used so you can understand what happens if the method modifies one of its arguments
- Pass by value, means copying the original objects, so the original object cannot be modified
- Assignment to a variable merely changes the binding; the object the variable referenced is not modified. Instead, a different object is bound to the variable
- Mutable objects can be modified without creating new objects
- Ruby is a pass by value for immutable objects, pass by reference otherwise

# Mutating and Non-Mutating Methods
- The receiver of a method call is the object on which the method is called. For instance, in foo.upcase, the receiver is foo.
- All methods are non-mutating with respect to immutable objects
- Assignment merely tells Ruby to bind an object to a variable
- treat = as a non-mutating method
- Assignment always binds the target variable on the left hand side of the = to the object referenced by the right hand side
- Setter methods for class instance variables and indexed assignment are not the same as assignment
- Setter methods and indexed assignment usually mutate their receiver
- Indexed assignment is mutating
- Some classes use << for "bit shift:" operations; such operations are usually non-mutating. Other classes may employ << for operations that have nothing to with bit shifts or appending; in those cases, you likely need to read the documentation or twest the operatino in a short program to determine if it's mutating or non-mutating
- Setters - they're methods that are defined to modify the state of an object
- Immutable objects aka passed by value
- Mutable objects seem to be passed by reference
- Assignment can break the binding between an argument name and the object it references

# Object Passing in Ruby
- Need to know what happens to the original objects passed to or returned from a method
- When you call a method with some expression as an argument, that expression is evaluated by ruby and reduced to an object
- Objects can be literals, named objects (variables and constants), or complex expressions
- Methods can include methods, blocks, procs, lambdas, and even operators
- Arguments can include actual arguments, the receiver of the method, operator operands, or a return value. (Loose use of terminology)
- Ruby uses strict evaluation exclusively, every expression is evaluated and converted to an object before it's passed along to a method
- Refer to pass by value and pass by reference as object passing strategies
- Most computer languages that employ strict evaluation use pass by value by default
- Developer needs to know what happens to the original objects passed to or returned from a method
- Passing the object to the method, aka object passing
- Receiver can be thought of as an implied argument
- Ruby also supports blocks, procs, and lambdas. All of these include the concepts of passing arguments and return values around
- Operators return values are passed around just like other methods
- Pass by Reference - if you modify the argument's state, you also modify the original object
- Ruby's variables don't contain objects; they merely reference to objects
- Pass by reference isn't limited to mutating methods
- A non-mutating method can use pass by reference as well
- Ruby variables and constants aren't objects, but are references to objects
- Assignment merely changes which object is bound to a particular variable
- Ruby is neither pass by value nor pass by reference, but instead employs a thirs strategy that blends the two strategies

## What Object Passing Strategy Ruby Uses:
- pass by reference value
- pass by reference
- Ruby acts like pass by value for immutable objects, pass by reference for mutable objects is a reasonable answer when learning about ruby, so long as you keep in mind that ruby only appears to act like this
