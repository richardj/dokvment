# Not this one!

Want to target one thing based on an unique identifier it has but don't want to keep on switching styles? Use the not pseudo class.

```
not(.classthing) {
  color: #666;
}
```

Make sure your selectors are correct so you don't do something to all elements except that one / few.


## Element divider

When you want to divide some elements you can whip out that specific template engine specific filter one that cuts up the array and adds comma's or pipes or whatever, but you can also use CSS

```
 .element:not(:last-child):after {
  content: " | ";
 }
```

Quite simple right? Just select the element that is not the last child and add a pipe.
