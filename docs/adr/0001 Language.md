# Language - Rust

What programming language to use?

# Problem

There are many possible programming languages. Here's the ones I considered:

* [Scala](https://scala-lang.org/) - I use this professionally and it is the language I am most comfortable with.
    * The strong typing is _awesome_, you can design away so many problems because you can trust the _compiler_ --
      before you even get to tests -- to prevent bad things from happening.
    * Unfortunately Scala -- being a JVM language -- isn't all that great for games. Don't get me wrong, it can be done
      and done well, but I do not enjoy writing the more contrived code that is typically necessary to minimize GC
      needs, and I do not want to debug those kind of problems when they appear.
* [C++](https://en.wikipedia.org/wiki/C%2B%2B) - While the most popular language for games, I haven't written in it
  since college, and while I admit it is evolved greatly, it would be
  a [large under taking to get back into into](https://www.learncpp.com/), and I'd still be doing manual memory
  management.
* [Go](https://www.learncpp.com/) - I did 2 years of Go professionally, and what I learned is that Go is great if you:
    * Are Google and are at the top of the dependency hierarchy
    * Like needing 4-lines to call _every_ function (can't forget to check for an error and return)
    * Want to claim there are no Exceptions...except you can `panic`, which can be "caught" using `defer` and handled
      using `defer` [Defer, Panic, and Recover](https://go.dev/blog/defer-panic-and-recover) ...
    * Still have to deal with `null`s like you would in C or Java
* [Rust](https://www.rust-lang.org/) - It sounds like the safety of Scala and the performance of C++. It's what I
  imagine Go wanted to be (and rightfully should have been -- if their language designer actually listened to the
  criticisms).

# Solution

[Rust](https://www.rust-lang.org/) for the win, and I hope it works out!

# Consequences

* It's a new language, still changing, with limited tooling and IDE support.
* Game engines in Rust new and untested, and often fancy wrappers around existing engines written in C or C++.
