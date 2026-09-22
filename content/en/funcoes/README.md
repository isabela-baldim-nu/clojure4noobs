# Functions

When we talk about functions we are talking about most of what a functional language does: *almost everything* is a function. A simple analogy: a box that takes an input, does some work inside, and returns an output.

![Black-box function example](https://www.researchgate.net/publication/230646848/figure/fig4/AS:669409437823002@1536611055840/Black-Box-function.png)

That is the idea. How do we declare a function in Clojure?

```clojure
(defn oi []
  (println "Oi!"))

(oi)

;; Result:
;;  Oi!
;;  nil
```

The structure is:
- `(`: start of a list
- `defn`: we are declaring a function
- `[]`: arguments/parameters (none in this case)
- `(println "Oi!")`: print the message "Oi!"
- `)`: end of the list
- `(oi)`: *invoke* the function

Functions always look like this: parameters go in square brackets and are used in the body. Here is a simple function that adds two values:

```clojure
(defn soma [a b]
  (println (+ a b)))

(soma 1 2)

;; Result:
;;  3
;;  nil
```
> Remember that `nil` is just the return value of `println`!

In this shape we take two parameters, add them, and print the result.

What if we want multiple arities — different behavior depending on how many arguments we get? We can!

```clojure
(defn testando-argumentos
  ([a] (println "Apenas um argumento foi enviado!"))
  ([a b] (println "Dois argumentos foram enviados!")))

(testando-argumentos 1) ;; Apenas um argumento foi enviado!

(testando-argumentos 1 2) ;; Dois argumentos foram enviados!
```

This is Clojure's way of handling functions that behave differently based on argument count!

What if we want unbounded arguments (like `+`)? Yes:

```clojure
(defn infinitos [& args]
  (println args))

(infinitos 1 2 3 4) ;; (1 2 3 4)
```

You receive a list of arguments and can work with each however you like! If you only care about the first one and still want to accept the rest:

```clojure
(defn infinitos-2 [primeiro & args]
  (println "O primeiro argumento foi " primeiro "\nOs demais são: " args))

(infinitos-2 1 2 3 4)

;; Result:
;;  O primeiro argumento foi  1 
;;  Os demais são:  (2 3 4)
;;  nil
```

Here we only treat the first argument; the rest stay as a list! To treat the second as well you could write `[primeiro segundo & args]`, and so on!

---

Great! With the basics of functions in place, we can move to something a bit magical: recursion!

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/funcoes/recursividade.md">Next -> Recursion</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
