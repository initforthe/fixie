# Fixie.js

Fixie is an open source tool that that automatically adds filler content to HTML documents. It's very simple, and we welcome contributions.

To learn more, check out  [fixiejs.com](http://www.fixiejs.com "fixiejs") 

### Why use Fixie?
When designing and developing websites, it's often useful to add lorem ipsum text to see what your page will look like without worrying about your final content.

Unfortunately, adding lots of filler content involves lots of copy-pasting and manual editing, and also makes your HTML unwieldy.

**Fixie.js** makes filler content succinct, making it faster and easier to test out your designs.

## Instructions

### Step 1 - Add fixie.js 

Add `<script type="text/javascript" src="fixie.js"></script>` to the bottom of your html document, right before your closing `</body>` tag.

### Step 2 - Add the `fixie` class.

Wherever you need filler content, set `class="fixie"`.

For example, if you wanted one filler paragraph, you could use
`<p class="fixie"></p>`

## Supported Elements
Fixie inserts the right type of content based on the tag name. Here are some major types you should be aware of:

- `<h1 class="fixie"></h1>` - Adds a few words of text. Same goes for `h2 - h6`
- `<p class="fixie"></p>` - Adds a paragraph of text.
- `<article class="fixie"></article>` - Adds several paragraphs of text.
- `<section class="fixie"></section>` - Adds several paragraphs of text.
- `<img class="fixie"></img>` - Adds an image which displays the width and height of the image.
- `<a class="fixie"></a>` - Adds a randomly named link.

## Fixie.init()

`fixie.init()` gives you fine-grained control over what fixie targets.

### selector
Select where you want filler content using CSS selectors.

Call
```
fixie.init({selector:[".array", "#of > .selectors", ".that", ".should", "#be > .populated", ".with", ".lorem"]}) 
```
or 
```
fixie.init({selector:".string, #of > .comma, .separated, .selectors, .that, .should, #be > .populated, .with, .lorem"})
```
in the JavaScript console or within a `<script>` tag.

### imagePlaceHolder
Use a different image placeholder service. By default, fixie uses http://placehold.it.

For example, to set the image placeholder to flickrholder.com, call
```
fixie.init({imagePlaceHolder: 'http://flickholdr.com/${w}/${h}/dslr'}) 
```

## Tips

### Add class fixie to containers
Fixxie will act on all child elements, but will never 
overwrite content within an element.

Consider the following example:
```
<div class="fixie">
<p>Hello <a></a></p>
</div>
```
Fixie will preserve the "Hello" text, but will
automatically add content to the link.

### Target empty elements
You can call Fixie on all empty elements on a page by calling:
```
fixie.init({selector:':empty'})
```
or by setting `<body class="fixie">`

### Flagging filler content
When you start adding real copy to your page, try adding the following CSS to your stylesheet:

`.fixie{ border:4px solid red; }`

This CSS will highlight all of your dummy content, making it easier to make sure you didn't miss anything.

## License

The MIT License

Copyright (c) 2012 Ryhan Hassan

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

