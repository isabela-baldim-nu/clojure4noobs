# When

`if` is a great conditional: first argument is the condition, second is the function to run when it is true, third is the function to run when it is not.

It would be nice to run several functions at once when a condition is true, right? That is what `when` is for!

```clojure
(when true
  (println "Testando 1")
  (println "Testando 2")
  (println "Testando 3")
  (println "Testando 4"))

;; Result:
;;  Testando 1
;;  Testando 2
;;  Testando 3
;;  Testando 4
;;  nil
```

Its main job is to take a condition and then run a series of expressions! Pretty handy, right?

---

`when` is neat. Ready for `cond`?

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/condicionais/cond.md">Next -> Cond</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
