Angular doesn't like IE8, when you get the warning
```
error: unexpected call to method or property acces
```

This probably means that you are using custom directives / custom elements.
IE8 will ignore those. Rebuilding your directives to attributes will fix that (at least for version 1.2.*)
