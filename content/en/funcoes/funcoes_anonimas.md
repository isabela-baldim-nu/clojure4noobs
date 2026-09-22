# Anonymous Functions

An anonymous function is a function that was not necessarily declared with a name — it is not bound to an identifier. They are often *passed as arguments to other functions*, *returned as values*, or used for a specific calculation (I will not spoil the next chapters too much).

A simple anonymous function looks like this:

```clojure
(def ola
  (fn [nome]
    (println "Olá," nome)))

(ola "He4rt Developers")

;; Result:
;;  Olá, He4rt Developers
;;  nil
```

The syntax is characteristic: `fn` defines it, it can take parameters (as above), and it is useful in many situations.

## Functions that return other functions

Anonymous functions unlock something magical: returning other functions to be computed later (I said I would not spoil it)!

Watch this:

```clojure
(defn multiplicar [multiplicar-por]
  (fn [n]
    (* n multiplicar-por)))

(def dobrando
  (multiplicar 2))

(dobrando 2) ;; 4

(def triplicando
  (multiplicar 3))

(triplicando 4) ;; 12
```

Here the anonymous function builds a new function that multiplies by a given number. Pretty cool, right?

---

How were anonymous functions? Next: general collection operations.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/manipulacoes">Next -> Collection operations</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
