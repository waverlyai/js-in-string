# js-in-string support for javascript in string literals

This very basic VSCode extension supports syntax highlighting file with the `.str.js` or `.str.ts` extensions which contains javascript, css or html code in backtick-quoted string literals. For example:

```javascript
export const code= /* js */ `
const x = 1;

export const f = (arr) => {
    arr.forEach((el) => {
        console.log(el);
    });
};
`;
```

(Naturally the code between the backticks shouldn't contain backtick-quoted strings.)

In the above code, the entire code between the backticks would be correctly syntax-highlighted by this extension.

Files of type `.str.js` are useful for embedding javascript code inside other javascript files, however without this extension, all the important code is highlighted as a string.

Other supported languages are CSS and HTML:

```javascript
export const cssCode= /* css */ `
p {
  color: red;
}
`;

export const htmlCode= /* html */ `
<html>
<body>
<p>Hello World!</p>
</body>
</html>
`;
```

## Features

Simple syntax highlighting.

![Syntax highlighting](images/syntax-highlighting.png)

## Release Notes

### 1.1.0

- Added support for CSS and HTML.
- Added support for .str.ts files.

### 1.0.0

Initial release of this extension.
