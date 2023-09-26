# Functional Programming and Purely Functional Programming

## Changing State in Functional Programming

Functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions and avoids changing state and mutable data. In functional programming, data structures are typically immutable, meaning once they are created, they cannot be modified. Instead of changing the state of a data structure, functional programming encourages creating new data structures with the desired changes, leaving the original data structures intact.

For example, if you have a list of numbers in a functional programming language like Haskell, and you want to add 1 to each number in the list, you would create a new list with the updated values, rather than modifying the original list.

```haskell
-- Functional approach
addOneToList :: [Int] -> [Int]
addOneToList [] = []
addOneToList (x:xs) = (x + 1) : addOneToList xs
```

## Purely Functional Programming

Purely functional programming takes functional programming a step further by adhering to the principle of referential transparency. In purely functional programming, functions have no side effects, and the output of a function depends only on its inputs. This means that purely functional programs are deterministic and can be easily reasoned about and tested.

In a purely functional program, you won't find features like mutable state, mutable variables, or global state changes. Instead, you work with immutable data and functions that create new data structures as needed.

## Differences from Other Programming Paradigms

Purely functional programming differs significantly from imperative programming, which is the predominant paradigm in languages like C++, Java, and Python. Imperative programs often involve changing the state of variables and data structures directly, which can lead to bugs and make code harder to reason about.

