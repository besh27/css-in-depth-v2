# Negative, Matching & Parent Selectors

## Negation Pseudo Class Selector
```
:not(li)
```
- negation
- select all elements that are no li's

```
div:not(.excludeThisClass)
```

### Safari Only Features
```
div:not(.a1, .a2)
div:not(.excludeThis):not(.excludeThisAlso)
```

## Matches
```
div:matches(.a1, .a2, .a3, .a4){}
```
- This matches any div element that has the the class of a1, a2, a3 or a4.
```
div:matches(#mainDiv) aside:matches(a:active)
```
- This matches any active anchor tags that are a decendant of the aside element that are also decendants of the div element with an id of mainDiv.

## Parent Selector (:has)
```
div:has(p)
```
- select all divs that have child p elements. 
- This approach is expensive because it will have to check all that div's decendents. 

___
Move on to [Linguistic Pseudo Class Selectors](07-linguistic-pseudo-classes.md)  
Back to [Selectors Main Page](00-selectors.md)