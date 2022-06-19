# Example with markup repl8ce tags

This example extends repl8ce tags, allowing you to tell templ8 that you want a tag to be parsed through a markup language first before being put on the output file. Simply prepend MD- or TX- to the name of a tag. MD will tell templ8 to use Markdown (which requires pandoc) and TX will use Textile.

Check out `input/index.textile`, `output/index.html`, `repl8ce`, and `basehtml`.
