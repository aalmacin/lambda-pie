# Addition operator implementation

Using `iter-Nat` to perform operation multiple times on a `Nat`

```
(claim + (-> Nat Nat Nat))
(define + (lambda (a b) (iter-Nat a b (lambda (x) (add1 x)))))
```

`(+ 3 4)` results in `(the Nat 7)`

In the background this is how it's evaluated

```
(iter-Nat 3 4 ( 
  (add1 (add1 (add1 4)))
))
```