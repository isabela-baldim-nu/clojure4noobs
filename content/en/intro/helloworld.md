# Hello World!

Now it is time for our first contact with Clojure! The classic "Hello World" could not be missing. Open your favorite editor and let's write some code.

## Printing to the screen

Create a file with the `.clj` extension. I named mine `hello_world.clj`... Remember that Clojure runs on the JVM, so you have access to almost every Java function (yes, that means interoperability)!

Enough talk — let's look at the code. We will go through the details later, so stay calm! Look at the snippet below:

```clj
(println "Hello World")
```

To try it, open a terminal and run:

```sh
$ clj hello_world.clj
```

You should see the message printed on the screen!

## Parentheses

You noticed that Clojure's syntax looks different from Java, right? The function that prints, `println`, still has the same name, even without `System.out` in front of it!

Why does the syntax look like this? Simple: Clojure follows Lisp ideas — prefix notation and lots of parentheses!

We will cover syntax in more depth later. For now, just make sure everything ran correctly!

---

You have taken your first step with Clojure. We can move on! How did it feel?

If you want to learn more about Lisp, I recommend the materials from [UFRN](https://www.dca.ufrn.br/~adelardo/lisp/) and [UFG](https://ww2.inf.ufg.br/~eduardo/lp/alunos/lisp/intro.html) (both in Portuguese)!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/intro/leiningen.md">Next -> Leiningen</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
