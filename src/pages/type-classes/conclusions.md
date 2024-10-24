## Conclusions

In this chapter we took a first look at type classes.
We saw the components that make up a type class:

- A `trait`, which is the type class

- Type class instances, which are given instances.

- Type class usage, which uses using clauses.

We saw that type classes can be composed from components using type class composition.
This is one form of metaprogramming in Scala, 
where we can get the compiler to do work for us based on our program's types.

We can view type classes as marrying codata with tools to select and compose implementations based on type. 
We can also view type classes as shifting implementation from the definition site to the call site.
Finally, can see type classes as a mechanism for ad-hoc polymorphism, allowing us to define common functionality for otherwise unrelated types.

Type classes were first described in @10.1007/3-540-19027-9_9 and @10.1145/75277.75283. @10.1145/1869459.1869489 details the encoding of type classes in Scala 2, and compares Scala's and Haskell's approach to type classes. Note that type classes are not restricted to Haskell and Scala. For examples, Rust's traits are essentially type classes.

As we have seen, Scala's support for type classes is based on implicit parameters (known as using clauses in Scala 3). Implicit parameters [@10.1145/325694.325708] were motivated by a desire to decompose type classes into smaller orthogonal language features, but they have been shown to be useful for other tasks. @10.1145/3360589 surveys different uses of implicits in Scala. See @OLIVEIRA_GIBBONS_2010 for a particularly mind-bending example. We'll see some of these different uses in later chapters.

Scala 3 has a few language features related to contextual abstraction that we haven't mentioned in this chapter. Context functions [@10.1145/3158130] allow functions to have using clauses. They are something the community is still exploring, and well defined use cases have yet to emerge. Generic derivation allows us to write code that generates type classes instances. Although this is extremely useful I think it's conceptually quite simple and doesn't warrant space in this book.
