## Haskell

- using [stack](https://docs.haskellstack.org/en/stable/README/) to compile/manage

- type `stack ghci` to get interactive session

- With emacs:

  - use [`haskell-mode`](https://github.com/haskell/haskell-mode);
    install with [melpa](https://melpa.org/) as explained in the
    ReadMe file for `haskell-mode`

  - use
    [`inf-haskell`](https://wiki.haskell.org/Emacs/Inferioar_Haskell_processes)
    for interactive session: put `(require 'inf-haskell)` in `.emacs`
    and then, with a `.hs` haskell file loaded in a buffer, use `C-c
    C-l` to get interactive session with that module automatically loaded.

- Use `:l myfile.hs` to load a file
- Use `:t object` to get the type of an object

---

```haskell
-- comments follow two hyphens
6 /= 3   -- not equal

-- define a function
doubleMe x = x + x

-- string = list of characters
['c', 'a', 't'] == "cat"

-- : operator to add to beginning of list
'c' : ['a', 't']

-- ++ operator to join two lists
['c'] ++ ['a', 't']

-- useful functions on lists
x = "karl has a cat"
head x
tail x
last x
init x
length x
null x
reverse x
take 5 x
drop 5 x
maximum x
minimum x
sum [3..10] -- integers 3 to 10
product [8,10..20] -- even numbers 8 to 20
'k' `elem` x -- contained in?
```