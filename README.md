# programming-language-idea-history
Tracing where features and concepts come from in programming languages

## List of languages to start with

* **Today's Big Three**: Java, JavaScript, Python
* **GC languages**: C#, Kotlin, D, Go, Nim, Zig, Scala, Clojure, Swift, Dart, Haxe
* **GC-less languages**: C, C++, Rust
* **FP languages**: Haskell, Racket, SML, OCaml, F#, Elm, PureScript
* **Scripting languages**: Lua, Julia, R, Ruby, Matlab, VBA, Groovy, PowerShell, Erlang, Perl, PHP, TypeScript
* **Declarative languages**: CSS, HTML, SQL
* **Forgotten languages**: Ada, Awk, HyperTalk, Modula-3, Self, Smalltalk, Oberon, Algol 60, Algol 68, Cobol, Fortress, BASIC, Simula, Oz, Prolog, Dylan, NewtonScript, Delphi, PL/I, APL, Rexx

## Wikipedia's list of languages

Wikipedia has [a footer template with programming languages](https://en.wikipedia.org/wiki/Template:Programming_languages), and I thought it was a nice representative list:

> Ada · ALGOL · APL · Assembly · BASIC · C · C++ · C# · Classic Visual Basic · COBOL · Erlang · Forth · Fortran · Go · Haskell · Java · JavaScript · Kotlin · Lisp · Lua · MATLAB · ML · Object Pascal · Pascal · Perl · PHP · Prolog · Python · R · Ruby · Rust · SQL · Scratch · Shell · Simula · Smalltalk · Swift · Visual Basic

Maybe the only thing I would contest is "Object Pascal" instead of Delphi, but that one is admittedly borderline.

## Link to a talk about `else`

[This talk](https://github.com/ericfischer/if-then-else/blob/master/if-then-else.md) is great, and lays out the history of if-else. [HN discussion](https://news.ycombinator.com/item?id=25406211).

## Link to C language history

[From the Internet Archive](https://web.archive.org/web/20080724200738/http://cm.bell-labs.com/who/dmr/chist.html).

In which I learn that the reason B and C use `break` (as opposed to a separate keyword like `endcase`) to escape out of `switch` statements, is that B was based on an older version of BCPL, before BCPL got the `endcase` keyword.

Interestingly, Perl 6/Raku re-introduced the difference with its `succeed` keyword.

## The separate compilation in ML was inspired by Modula

See https://github.com/masak/interesting-papers/issues/450 for details.

## Nim was inspired by Modula/Oberon

Its type and module systems were, according to [this HN thread](https://news.ycombinator.com/item?id=26275553).

## Timeline from Wikipedia

[This timeline](https://en.wikipedia.org/wiki/Timeline_of_programming_languages) is a great resource and starting point for choosing influential languages.

## Where does `for` come from?

According to [Wikipedia](https://en.wikipedia.org/wiki/Superplan),

> Superplan introduced the keyword "for" resp. the German
> [für](https://en.wiktionary.org/wiki/f%C3%BCr#German)
> with its [for loop](https://en.wikipedia.org/wiki/For_loop)

## Internal and external iterators

Two blog posts ([one](https://journal.stuffwithstuff.com/2013/01/13/iteration-inside-and-out/), [two](https://journal.stuffwithstuff.com/2013/02/24/iteration-inside-and-out-part-2/)) by Bob Nystrom give a pretty good overview.

* _External_ iterators tend to look like `Iterable`/`Iterator` interfaces, and a `for` loop syntax
* _Internal_ iterators tend to look like an `each` or `forEach` method

## Dijkstra's famous argument for half-open intervals

[Why numbering should start at zero](https://www.cs.utexas.edu/users/EWD/transcriptions/EWD08xx/EWD831.html) argues both for counting from zero, and for using half-open intervals (like Python does).

## A history chart

The paper [Programming Languages: History and Future](https://dl.acm.org/doi/pdf/10.1145/361454.361485) has an _awesome_ history chart on page 6.
It's hard to do this chart justice.
All the languages that survived to the present day are there, and a great many others besides.

## Short-circuiting boolean operators

* Dijkstra famously [warned against](https://www.cs.utexas.edu/users/EWD/ewd10xx/EWD1009.PDF) short-circuiting logical operators, but in practice they are widespread in modern languages.
* A number of languages have both the non-short-circuiting form and the short-circuiting form.
* In more than one BASIC, `AND` and `OR` do not short-circuit.

## Type punning and the "truthy" convention

We should discuss this. A number of mainstream languages follow this convention:

* Perl 5/Raku
* Python
* JavaScript

Many others don't.
It influences how you write conditions in the language, and spreads into other nearby idioms.
