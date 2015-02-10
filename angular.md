Angular doesn't like IE8, when you get the warning
```
error: unexpected call to method or property acces
```

This probably means that you are using custom directives / custom elements.
IE8 will ignore those. Rebuilding your directives to attributes will fix that (at least for version 1.2.*).

If you need to support IE8, refrain from using element directives, because it is a huge hassle, just refrain from using custom stuff altogether and focus your energy on minimizing IE8 use.
