## Check if Object

Checking wether something is exists is a little bit harder in Javascript than for instance in PHP where you can just do something like if (isset(thing)).
But there are ways apparently.

```
if (typeof obj.foo != 'undefined') {
    // ..
}
```
source: http://stackoverflow.com/questions/2281633/javascript-isset-equivalent

## Get tree depth

Getting the tree depth of your data source, for when you need it.


```
getDepth = function (obj) {
    var depth = 0;
    if (obj.children) {
        obj.children.forEach(function (d) {
            var tmpDepth = getDepth(d)
            if (tmpDepth > depth) {
                depth = tmpDepth
            }
        })
    }
    return 1 + depth
}
```
