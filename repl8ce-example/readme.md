# Example with repl8ce tags

This example showcases another fundamental feature of templ8: The repl8ce tags. A repl8ce tag is composed of keys and values. The keys are like the names of the tags, and the values are the content that they put in a page.

The default values of every key *must* be set in the repl8ce file, to avoid causing errors. You can set a value to be an empty string.

The syntax for setting values is simple, and the same across the entire project:

```
KEY=VALUE
;;KEY2
Multi
Line
Value
```

KEY is a single-line key, while KEY2 is a multiline key. Multiline keys *must* be after every single-line key.

To set the values of a specific file's keys, use the same syntax and put `-BEGINFILE-` after all the tags are set. The content of your file must go after `-BEGINFILE-`

When using `templ8 divine`, templ8 will replace ``##KEY`` and ``#KEY2`` with their respective values. It will *not* surround them with HTML tags, so that must be done in the base template file.

It's also possible to make a file called `repl8ce` in any directory in `input` for those to be the values set for every file in that directory (non-recursive).

Check out `input/index.textile`, `output/index.textile`, `repl8ce` and `basehtml`.
