# self-contained hacky Bash formatter
Abusing Bash pretty-printing of parsed functions to format scripts. Who needs reliable tools like [`shfmt`](https://github.com/mvdan/sh)?

## Caveats
- If the input has syntax errors like a mismatched `}`, it'll **run part of the input** instead of formatting it!
- Comments are deleted. Though, I'm considering to somehow track their line-numbers and re-insert them.
- Fails on tab-indented here-docs (`<<-`)
