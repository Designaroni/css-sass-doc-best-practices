# css-sass-doc-best-practices
Best Practices for CSS and SASS, Sassdoc, general/personal best practices

Examples:
---

### Indentation:

**Rule:** 2 spaces over tabs or 4 spaces.

**Why:** Every character counts, even spaces, minimize your code as much as possible while maintaining syntax & structural order. When you write less code interpreters & preprocessors have less work to do. To the naked eye, when file widths from L to R are minimized more code is visible & scannable in a code editors viewport at a single time.

---

### Code Commenting:

**Rule:** Start your files with a code comment

**Why:** For clarity. Name the file, describe the purporse and additional file references as needed

```
/**
 * CSS or SASS Component Title
 * @description - CSS Styles for component that does X, Y, and Z. Enables new functionality in theme.
 * @requires {Content Management Settings}
 * @requires {_file_name.js}
 * @see - {_file_name.js}
 * example - ...
 */
```


**Rule:** Leave a space above inline comments when describing a CSS chain declaration 

**Why:** For visual flow, allows visual cadence between comments without cluttering the files syntax structure

```

// inline comment, note the space above the inline comment
.cssClass {
  property:value;
}
```

**Rule:** Inline comments inside of a CSS chain declaration should maintain empty line return, may have a start and end, may also be written preceding the closing `;` of a property

```
.cssClass {
  // Manually adding padding
  padding-top: 5px;
  padding-right: 10px; 
  padding-bottom: 5px;
  padding-left: 10px;
  font-size: 42px;
  line-height: 42px; // line-height should be kept in sync with font-size property
  font-weight: 400;
  // Color variable used for text should stay in sync with @mixin typography-colors
  color: $color-gray-dk-5;
  // end
}
```

---

### Syntax Rules:

**Rule:** Write CSS long hand in the order rendered by thier shorthand counterpart ex: padding: <top> <right> <bottom> <left>;

**Why:** Not only does this follow Web Doc Standards but this style of coding acts and a mnemonic device, writing long hand helps you remember the short hand order, writing short hand helps you remember the long hand property names & available values. 

```
// short hand:
padding: 0px 2px 4px 6px;
// long hand variant:
padding-top: 0px;
padding-right: 2px;
padding-bottom: 4px;
padding-left: 6px;
```

**Rule:** Write CSS, SASS (or other interpreted CSS languages) to follow the order of the DOM HTML or JS template component

**Why:** Keeps your code clean, let your HTML describe your CSS and CSS desceribe your HTML. Less mess, less fuss, less brain power needed to interpret the order of code
  
