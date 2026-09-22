# Cond

We have seen how to run a larger block when a condition is true. What about checking several conditions, each with its own body?

Meet `cond` with a simple example: multiple conditions...

```clojure
(let [n 10]
  (cond
    (> n 0) (println "O número é positivo!")
    (< n 0) (println "O número é negativo!")
    :else (println "Ok, o número não é positivo nem negativo...")))

;; Result:
;;  O número é positivo!
;;  nil
```

With `cond` we can run different expressions for different checks, keeping complex conditions readable. The only extra detail is `:else`, which should be the last clause — the fallback when none of the others matched!

---

`cond` is quite useful in real projects. Our last conditional in this chapter is `case`.

<p align="right">
  <a href="https://github.com/lanjoni/clojure4noobs/tree/main/content/en/condicionais/case.md">Next -> Case</a>
</p>

<p align="left">
  <a href="https://github.com/lanjoni/clojure4noobs/blob/main/README.en.md#roadmap">Back to the main menu</a>
</p>
