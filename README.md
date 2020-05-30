# Python parsers
This page lists a few Python parsers. May it be of help for those looking for the right tool.
## lossless
### LibCST
* https://github.com/Instagram/LibCST
* Maintained by Instagram
* keeps all formatting details (comments, whitespaces, parentheses, etc)
* looks and feels like an AST
### Baron
* https://github.com/PyCQA/baron
* ull Syntax Tree (FST) library
* keeps everything and guarantees the operation `fst_to_code(code_to_fst(source_code)) == source_code`
* used in [RedBaron](https://github.com/PyCQA/redbaron)
### tokenize
* https://docs.python.org/3/library/tokenize.html
* a lexical scanner for Python source code
* returns comments as tokens as well
* useful for implementing “pretty-printers”
## lossy
### ast
* https://docs.python.org/3/library/ast.html
## not sure
### parso
* https://github.com/davidhalter/parso
* supports error recovery 
* supports error recovery and round-trip parsing for different Python versions (in multiple Python versions).
* battle-tested by [jedi](https://github.com/davidhalter/jedi) (pulled out of jedi to be useful for other projects)
### Astroid
* https://github.com/PyCQA/astroid
* a common base representation of python source code.
* powering [pylint](https://www.pylint.org/)
* provides a compatible representation which comes from the _ast module (builds an extended ast)
* include some support for static inference and local name scopes
* can also build partial trees by inspecting living objects
### horast
* https://github.com/mbdevpl/horast
* Human-oriented abstract syntax tree (AST) parser/unparser for Python 3 that doesn't discard comments
* based on built-in tokenize module, as well as community packages asttokens and typed_ast
## refactoring
### Rope
* https://github.com/python-rope/rope
* a python refactoring library
### `lib2to3`
* https://docs.python.org/3/library/2to3.html
* reads Python 2.x source code and applies a series of _fixers_ to transform it into valid Python 3.x code
### Bowler
* https://github.com/facebookincubator/bowler
* a refactoring tool for manipulating Python at the syntax tree level
## Texts
### `tokenize` vs. Alternatives
* https://www.asmeurer.com/brown-water-python/alternatives.html
* discusses `tokenize`, `ast`, regular expressions, and Parso.
