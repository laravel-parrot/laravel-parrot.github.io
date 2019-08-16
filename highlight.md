* https://github.com/markedjs/marked/blob/master/docs/USING_ADVANCED.md

* https://github.com/highlightjs/highlight.js/blob/master/src/styles/atom-one-dark.css

```js
// Create reference instance
const marked = require('marked');

// Set options
// `highlight` example uses `highlight.js`
marked.setOptions({
  renderer: new marked.Renderer(),
  highlight: function(code) {
    return require('highlight.js').highlightAuto(code).value;
  },
  pedantic: false,
  gfm: true,
  breaks: false,
  sanitize: false,
  smartLists: true,
  smartypants: false,
  xhtml: false
});

// Compile
console.log(marked(markdownString));
```



