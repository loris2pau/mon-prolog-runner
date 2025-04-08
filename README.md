# prolog-runner README

This is a **fork** of the original prolog-runner extension, with a modification to the command that removes the `-t halt` option.

The original extension runs your Prolog code like a script using the following command:
``swipl -q -f ${file} -t halt.``

In this fork, the `-t halt` option has been **removed**, so the command will look like this:

``swipl -q -f ${file}``


This allows you to run your Prolog code without forcing it to halt after execution, which is useful for scenarios where you want to keep the Prolog environment open for further interaction or debugging.

The extension requires **swipl** to be in your PATH.

![screenshot](https://raw.githubusercontent.com/sazzledazzle/prolog-runner/main/screenshot.png)

Because the default language assignment for `.pl` files is Perl, you may need to change the language to Prolog manually in the bottom right corner:

![Change Language to Prolog](https://raw.githubusercontent.com/sazzledazzle/prolog-runner/main/change_lang.png)

## Example

Just add the `initialization/1` predicate to your file (see https://www.swi-prolog.org/pldoc/man?predicate=initialization/1).

e.g.:
```prolog
:- initialization run.

run :- write('Hello, this is a simple Prolog program!').
```

License MIT