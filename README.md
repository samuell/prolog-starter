# Starter Template for SWI-Prolog Projects

Before proceeding with the instructions below, be sure to download and install [SWI-Prolog](https://www.swi-prolog.org/Download.html).  Note, for MacOSX, I prefer to use [Homebrew](https://formulae.brew.sh/formula/swi-prolog) instead.

## Instructions

To convert this template to your own project:
1. Replace the word *starter* with the name of your main program in both `Makefile` and `load.pl`.
2. Replace `src/starter.pl` with your own main program.
3. Replace `src/starter.plt` with your own main program and write some tests.
4. Use `make <target>` where `<target>` is either `test`, `cov` or `repl`, to compile and run your program.

## License
Licensed under the MIT license which can be found in the file
`LICENSE` in the project root.

## References

1. [Prolog Unit Tests](https://www.swi-prolog.org/pldoc/doc_for?object=section(%27packages/plunit.html%27))
2. [SWI-Prolog Source Documentation Infrastructure](https://www.swi-prolog.org/pldoc/doc_for?object=section(%27packages/pldoc.html%27))

## Coding Guidelines

 * Use empty imports (use_module(mymodule, [])) in order to not
   pollute the namespace.
 * Always use module prefixes (mymodule:predicate(...)) in order to
   clarify where things are coming from.
 * Always use the "made-up" module prefix "core:" when calling
   built-in predicates. This is completely unnecessary, and doesn't even
   work in all cases, but I think it is a good idea as long as it doesn't
   cause any problems. This decision may need to be revised when
   compatibility between different Prologs is investigated.
 * Avoid the if-then-else construct. It just looks ugly.
 * Avoid disjunctions. They are ugly, and can be replaced by properly
   written helpers. Think: premises are "and", clauses are "or".
 * Use cuts where appropriate, and try to keep each cut on a line by
   itself unless its placement is obvious and consistent in each clause.
   PlUnit is excellent at pointing out when tests succeed but leave
   choice points.
 * Try to avoid spaces within lists and structures, but always use
   spaces between arguments.
 * Predicates, atoms, etc. should use "this_naming_style" while variables
   should use "ThisNamingStyle".
 * Try to stick to the PlDoc structure.
 * If in doubt, consult: [Some Coding Guidelines for Prolog](https://www.cmpe.boun.edu.tr/sites/default/files/prolog_coding_guidelines.pdf)
 
## Credits
 The structure of this starter template was modeled after a prolog project by [khueue](https://github.com/khueue/prolog-json).
