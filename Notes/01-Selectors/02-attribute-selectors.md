# Attribute Selectors

CSS2 introduced several attribute selectors. These allow for matching elements based on their attributes. CSS3 expands upon those attribute selectors, allowing for some targeting based on pattern matching. CSS Selectors Level 4 adds a few more:

- [CSS1 Attribute Selector](#css1-attribute-selector)
- [CSS2 Attribute Selectors](#css2-attribute-selectors)
- [CSS3 Attribute Selectors](#css3-attribute-selectors)

## CSS1 Attribute Selector

```
element[attr]
```

Matches any element E that has the attribute attr regardless of the attribute’s value. We made use of this back in Chapter 4 to style required inputs; input:required works in the latest browsers, but input[required] has the same effect and works in IE7 and IE8 as well.


## CSS2 Attribute Selectors

```
element[attr=val]
```

Matches any element E that has the attribute attr with the exact value val. While not new, it’s helpful in targeting form input types; for instance, targeting checkboxes with input[type=checkbox].

```
element[attr|=val]
```

Matches any element E whose attribute attr either has the value val or begins with val-. This is most commonly used for the lang attribute. For example, p[lang|="en"] would match any paragraph that has been defined as being in English whether it be UK or US English with &lt;p lang="en-uk"> or &lt;p lang="en-us">.

```
element[attr~=val]
```

Matches any element E whose attribute attr has within its value the full word val, surrounded by whitespace. For example, .info[title~=more] would match any element with the class info that had a title attribute containing the word “more,” such as “Click here for more
information.”

## CSS3 Attribute Selectors

```
element[attr^=val]

/* example */

a[href^=mailto] {background-image: url(emailicon.gif);}
a[href^=http]:after {content: " (" attr(href) ")";}

```
Matches any element E whose attribute attr starts with the value val. In other words, the val matches the beginning of the attribute value.


```
element[attr$=val]

/* example */

a[href$=pdf] {background-image: url(pdficon.gif);}
a[href$=pdf]:after {content: " (PDF)";}
```
Matches any element E whose attribute attr ends in val. In other words, the val matches the end of the attribute value.

```
element[attr*=val]
```
Matches any element E whose attribute attr matches val anywhere within the attribute. It is similar to element[attr~=val], except the val can be part of a word. Using the same example as before, .fakelink[title*=info] {} would match any element with the class fakelink that has a title attribute containing the string info, such as “Click here for more information.”

In these attribute selectors, the value of val is case-sensitive for values that are case sensitive in HTML. For example, input[class^="btn"] is case sensitive as class names are case sensitive, but input[type="checkbox"] is not case sensitive, as the type value is case-insensitive in HTML.

The value does not have to be quoted if the value is alphanumeric, with some exceptions. Empty strings, strings that begin with a number, two hyphens, and other quirks need to be quoted. Because of the exceptions, it’s a good idea to make a habit of always including quotes for those times when you do need them.

In CSS Selectors Level 4, we can have case insensitivity by including an i before the closing bracket, 
```
element[attr*=val i].

/* example */

input[type=checkbox i]

```

___
Move on to [User Interface Selectors](03-user-interface-selectors.md)  
Back to [Selectors Main Page](00-selectors.md)