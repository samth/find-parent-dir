# Finding containing directories

This package provides utilities for examining parent
directories.  As an example, `git` looks for a `.git`
directory in any parent directory of the current
directory.  That would be expressed here as:

    (find-parent-containing (current-directory) ".git")

## Exports

```
(find-parent-containing [start path-string?] [sentinel path-string?]) -> (or/c #f path?)
```

Finds a parent directory of `start` that contains `sentinel`, or returns `#f`.

```
(find-parent-dir [start path-string?] [pred (-> path? any)]) -> (or/c #f path?)
```

Finds a parent directory of `start` that matches `pred` or returns `#f`.
