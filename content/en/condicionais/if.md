# If

You will find `if` in many languages. Its main job is to take a path when a condition is true, or an alternative path when it is not.

Clojure's `if` looks a bit different because everything is a function that takes arguments. A well-known `if` in other languages might look like:

```javascript
if (condicao) {
  // Do something
} else {
  // Do something else
}
```

In Clojure it works a little differently:

```clojure
(if (> 1 2)
    (println "1 é maior que 2")
    (println "1 não é maior que 2"))

;; Return:
;;  1 não é maior que 2
;;  nil
```

The shape is easy to follow: `(if (condicao) (then-branch) (else-branch))`, with inner functions for each branch.

We could go further:

```clojure
(def a 5)

(if (< a 0)
    (println "Menor que 0")
    (if (= a 0)
        (println "Igual a 0")
        (println "Maior que 0")))

;; Return:
;;  Maior que 0
;;  nil
```

To simplify, we can use a local binding with *let*:

```clojure
(let [a 5]
  (if (< a 0)
    (println "Menor que 0")
    (if (= a 0)
        (println "Igual a 0")
        (println "Maior que 0"))))

;; Return:
;;  Maior que 0
;;  nil
```

Here *let* binds a value to a *variable* in the same context — it stays in the scope where it was declared!

What if we want more than one expression in a branch? Use `do`:

```clojure
(if (> 1 2)
    (do
      (println "Epa, recebi seus valores!")
      (println "Pelo que parece 1 é maior que 2!"))
    (do
      (println "Epa, recebi seus valores aqui hein!")
      (println "Pelo que parece 1 não é maior que 2!")))

;; Return:
;;  Epa, recebi seus valores aqui hein!
;;  Pelo que parece 1 não é maior que 2!
;;  nil
```

---

What did you think of `if`? Let's meet `when`.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/condicionais/when.md">Next -> When</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
