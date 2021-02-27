# lit-glob

A file globbing library for Luvit.
## Functions



| Element | Summary |
|---------|---------|
| **Functions** |  |
| [compile](#compile) | Compiles a glob string into a Lua pattern for use in matching files. |
| [match](#match) | Checks if `file` matches `glob` after prepending `dir`. |
| [match_baseless](#match_baseless) | Checks if `file` matches `glob`. |
| [readdir](#readdir) | Iterates recursively over `dir` and returns a table of all files matching `glob`. |
| [scandir](#scandir) | An iterator which will iterate recursively over `dir` and return the `path` and `kind` of each matching file. |

### compile

**Type:** `str:string -> pattern:string`  

Compiles a glob string into a Lua pattern for use in matching files.



### match

**Type:** `dir:string, file:string, glob:string -> matches:boolean`  

Checks if `file` matches `glob` after prepending `dir`.

`file` should be a path starting with `dir`.

### match_baseless

**Type:** `file:string, glob:string -> matches:boolean`  

Checks if `file` matches `glob`.



### readdir

**Type:** `dir:string, glob:string -> files:table`  

Iterates recursively over `dir` and returns a table of all files matching `glob`.



### scandir

**Type:** `dir:string, glob:string -> iterator:function`  

An iterator which will iterate recursively over `dir` and return the `path` and `kind` of each matching file.

This is intended for use in `for path, kind in` statements, but may be used individually.
`path` will be relative to `dir.
`kind` will be one of `file`, `directory`, or any other possible file type.
