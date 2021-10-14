# Neν
A New Language.

The language is given the name Neν because

- It is a **new** language, as both the last greek letter **ν** and the full name Neν (mimicing New) suggests.

- It does not intend to be a huge language which incorporates every modern and fancy feature; instead, it will be kept **simple and incomplete**. as the one ν cannot forms the complete word Neνν.

## Design Philosophies

I would like to first write down some design philosophies (or trade-offs, more frankly) here. Based on these design philosophies, we may know what tasks are suitable for this language.

1. Performance will always not be the primary goal, or even not be one of the goals at all.
2. The language shall be **data-centric and data-driven**, instead of being imperative. The programmer shall focus on constructing and transforming datas. If necessary, remove imperative constructs to aid the goals.
3. Variables shall be **immutable by default**; (local) mutable variables are an implicit optimisation that will be done whenever possible. (Could provide mutable variables, whose types, however, will be distinc from the immutable ones.)
4. Types and their values shall have a **uniform representation by default** (ie, heap-allocated); optimisation will be done implicitly whenever possible.
5. The language shall take in charge of **memory allocation and reclamation**. Programmers shall pay zero attention to the issue.
6. Local **type annotations shall be ommitted** but always possible for all declarations (and expressions).
7. The language shall have a simple yet powerful **core language**.
8. The language shall **focus on the frontend**, and use code-to-code translation to some existing languages or IRs.
9. The language shall provide an easy way to write **parallel programs and concurrent programs**.
10. Do not handle numeric values, arithmetic expressions, and overflow from scratch; reuse existing ones instead.
11. No inheritance. Even if it has inheritance, the inheritance does not lead to subtyping.
12. The language shall support **row polymorphism**.
13. If it supports subtyping, it must (also) support **structural subtyping**.

## Questions to Answer

1. Is variance usefull at all? Is the combination of definition-site variance and use-site variance usefull at all?
2. Is complex function overloading usefull at all? Can we use only intersection types or some other techniques?
3. Is exceptions and their try-catch useful at all?
4. Is subtyping only (no typing) feasible?

## Techniques to master

1. Elaboration: from the surface language to the fully-typed core language.
2. Data representation: compile and translate polymorphic functions and types. Autoboxing algorithms.(Omitted if translated to some other languages already having the features.)
3. Garbage collections. (Omitted if translated to some other languages already having the features.)
4. Treat of infix operator overloading.
5. Compilation of pattern matching expressions.
6. Exhaustiveness checks.
7. Tag elimination and partial evaluation.
