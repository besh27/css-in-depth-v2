# Structural Selectors 

## Available Selectors
```
:root  
:empty  
:blank  
:nth-child()  
:nth-last-child()  
:first-child*  
:last-child  
:only-child  
:nth-of-type()  
:nth-last-of-type()  
:first-of-type
:last-of-type
:only-of-type
```

These selectors target elements on the page based on their relationships to other elements in the DOM.

Updates dynamically if page updates.

[Practice Here:](https://estelle.github.io/cssmastery/selectors/files/04_firstlastonly.html) 


## nth pseudo-classes
```
:nth-child(3)
:nth-child(3n) /* if this is iterated over */  
:nth-last-child(odd)  
:nth-child-type(5)
:nth-last-of-type(3n+1)
```
These taret element or elements based on the argument passed to the selector.  

Below are soem examples:
```
li:first-child,
li:last-child {
  font-weight: bold;
}
li:first-of-type,
li:last-of-type{
  text-decoration:line-through;
}
li:nth-child(even) {
  background-color: #CCC;
}
li:nth-child(3) {
  color: #CCC; /* gray */
}
li:nth-of-type(odd) {
  background-color: #FFF; 
}
li:nth-of-type(4n) { /* every 4th element of this type */
  color: hsl(205, 87%, 50%);
}

li:nth-of-type(3n-1){ /* 2, 8, 11 ... this is an An+B equation. */
    text-align: right;
}
```

___
Move on to [Root, Empty & Blank Selectors](05-root-empty-blank.md)  
Back to [Selectors Main Page](00-selectors.md)