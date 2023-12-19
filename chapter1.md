# Introduction

## Functional vs. Imperative Data Structures

- > First, from the point of view of designing and implementing efficient data structures, functional programming's stricture against destructive updates (i.e., assignments) is a staggering handicap, tantamount to confiscating a master chef's knives. Like knives, destructive updates can be dangerous when misused, but tremendously effective when used properly.
  
- *persistent* data structure - supports multiple versions

    *ephemeral* - allows only a single version at a time

- > In light of all these points, functional data structures sometimes seem like the dancing bear, of whom it is said, "the amazing thing is not that [he] dances so well, but that [he] dances at all!" In practice, however, the situation is not nearly so bleak.

## Strict vs. Lazy Evaluation
- strict languages: the arguments to a function are evaluated before the body of the function;
lazy languages: arguments are evaluated in a demand-driven fashion; they are initially passed in unevaluated form and are evaluated only when (and if!) the computation needs the results to continue; once a given argument is evaluated, the value of that argument is cached -> if it is ever needed again, it can be looked up rather than recomputed (this caching is known as *memoization*)

- strict languages: can describe worst-case data structures, but not amortized ones;
lazy languages: can describe amortized data structures, but not worst-case ones

## Terminology

- data structure as:
  1. **an abstraction**: an abstract data type (a type and a collection of functions on that data type)
  2. **an implementation:** a concrete realization of an abstract data type
  3. **an object / a version:** an instance of a data type (such as particular list or tree)
  4. **a persistent identity:** a unique identity that is invariant under updates;
    different versions of the same data structure *share a common persistent identity*;
    the persistent identity of an ephemeral data structure can be reified as a reference cell, but this approach is insufficient for modelling the persistent identity of a persistent data structure