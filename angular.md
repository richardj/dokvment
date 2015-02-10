Angular doesn't like IE8, when you get the warning
```
error: unexpected call to method or property acces
```

This probably means that you are using custom directives / custom elements.
IE8 will ignore those. Rebuilding your directives to attributes will fix that (at least for version 1.2.*).

If you need to support IE8, refrain from using element directives, because it is a huge hassle, just refrain from using custom stuff altogether and focus your energy on minimizing IE8 use.

## Hidden inputs

Sometimes you want to send a form like a regular old form, you know, hidden inputs with values you check and want to have available. Of course with Angular you don't really need that,
but development is never as straight-forward as the documentation wants you to believe and Angular will ignore hidden things. An ng-value attribute will fix this!

Just do something like:

```
<input type="hidden" name="someData" ng-value="data" />
```

And you should be good to go! Found of course on [stackoverflow](http://stackoverflow.com/questions/18446359/angularjs-does-not-send-hidden-field-value)
