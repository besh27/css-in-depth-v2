# Selectors

## Basic Selectors
- ID
- Class
- Element

Good rules to follow:
- Always start with broad styles.  
- when targeting an element, target the lowest element specificity as possible.

## CSS Selectors
### CSS 1
- Element
- Decendents ' ', which is a combinator. (example: 'li a')
- Class .class
- ID #IDName
- Link :link
- Active :activeLink

### CSS 2
- All *
- Direct Child >
- Adjacent Sibling + (element that comes immediately after)
- element[attribute]
- element[attribute=value]
- element[attribute~=value]
- element[attribute|=value]
- :first-child
- :lang(en)
- :focus
- :hover
- :visited
- :before
- :after
- :first-letter
- :first-line

### CSS 3
- ::before
- ::after
- ::first-letter
- ::first-line
- element[attribute^=value]
- element[attribute$=value]
- element[attribute*=value]
- element ~ element
- :root
- element:last-child
- element:only-child
- element:nth-child(n)
- element:nth-last-child(n)
- element:first-of-type
- element:last-of-type
- element:only-of-type
- element:nth-of-type(n)
- element:nth-last-of-type(n)
- element:empty
- element:not(selector)
- element:target

### UI / Selectors #4

- element:enabled
- element:disabled
- element:checked
- element:default
- element:valid
- element:invalid
- element:in-range
- element:out-of-range
- element:required
- element:optional
- element:read-only
- element:read-write

### More Level 4 Selectors (some may not be supported)
- :selection
- :scope-context()
- :current(s)
- :past
- :future
- :host
- :host()
- :host-context()
- ::shadow
- ::context


## Specificity: How it works

- 1-0-0: ID Selector
- 0-1-0: Class/pseudoClass selectors
- 0-0-1: Element Selector

## Specificity and Cascade. 

If an element has a high specificiy 'score' and a similar style later in the cascade, the later one will take precedence. 