# Relational Selectors

## Descendant Selector
    This selector selects all children regardless of the distance from the parent. 
- ul li
    - this example will select all li elements under all the ul elements. 
- ol li
- div p

## Child Selector
    E > F
    This selector matches any element F that is a direct child of element E - any further nested elements will be ignored. 
- ul > li
- ol > li
- p > a

## Adjacent Sibling Selector
    E + F
    This will match any element F that shares the same parent as E and comes directly after the E in the markup. 
- li.hasaclass + li
- div.hasaclass + div

## General Sibling Selector
    E ~ F
    This will match any element F that shares the same parent as any E and comes after it in the markup.
- ul ~ li
- Targets the elements after an element. 
___
Move on to [Attribute Selectors](02-attribute-selectors.md)  
Back to [Selectors Main Page](00-selectors.md)