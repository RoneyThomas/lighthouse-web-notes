### isInstanceOf vs Array.isArray()

typeof for arrays returns "object":

```javascript
typeof([]) // => "object"
```

Indeed an array is technically an object, though most of the time, we don't need to think of it that way. However, the real problem here is that the same output happens for all objects, including objects that are definitely not arrays!

```javascript
typeof({}) // => "object"
```
While "object" does help us separate array data from other types like strings, numbers, and the like, it doesn't give us complete confidence that we're dealing with an array here.

Array.isArray overcomes this confusion by being a more specific check.