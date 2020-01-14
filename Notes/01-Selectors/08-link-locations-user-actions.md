# Linguistic Pseudo Class Selectors

```
:link
:visited
```

- a with an href attribute

## CSS Selectors Level 4

```
:any-link
:matches(:link, :visited)
```

- these are the same.

## User Action Pseudo Classes

```
:hover
:active
:focus
```

- When using active or focus, use them at the same time. they are for different use cases. This is because some people use the mouse, some people will interact with the interface via the keyboard.

```
a:visited:hover
button:active:focus
```

## More User Action PC Selectors

```
:focus-ring
:focus-within
:drop
:drop()
```

## Drag and Drop Pseudo Classes

```
:drop
```

- drop argets while the user is "dragging". The 'dropzone' attribute is not yet supported ,thus rendering this useless...

```
:drop(active)
:drop(valid)
:drop(invalid)
```

- current drop target for the drag operation.
- drop target is valid or the object currently being dragged, like correct filetype.
- drop target is invalid for the object currentl being dragged.

## Target

```
:target

myPage.html#anchor

<div id="anchor">stuff</div>

div:starget::first-line {
    font-weight: bold;
}

```

### Example with styling tables

```
section:not(:target) > a {
  background-color: #ccc;
}
section:target > a {
  background-color: white;
  border-bottom-color: #fff;
}
section:not(:target) > div { z-index: -2; }
section:target > div { z-index: -1; }
```

---

Move on to [Specificity](09-specificity.md)  
Back to [Selectors Main Page](00-selectors.md)
