---
title: Style.builtIn property
linktitle: builtIn property
articleTitle: builtIn property
second_title: Aspose.Words for NodeJs
description: "Style.builtIn property. True if this style is one of the built-in styles in MS Word."
type: docs
weight: 40
url: /nodejs-net/aspose.words/style/builtIn/
---

## Style.builtIn property

True if this style is one of the built-in styles in MS Word.


```js
get builtIn(): boolean
```

### Examples

Shows how to differentiate custom styles from built-in styles.

```js
let doc = new aw.Document();

// When we create a document using Microsoft Word, or programmatically using Aspose.words,
// the document will come with a collection of styles to apply to its text to modify its appearance.
// We can access these built-in styles via the document's "Styles" collection.
// These styles will all have the "BuiltIn" flag set to "true".
let style = doc.styles.at("Emphasis");

expect(style.builtIn).toEqual(true);

// Create a custom style and add it to the collection.
// Custom styles such as this will have the "BuiltIn" flag set to "false". 
style = doc.styles.add(aw.StyleType.Character, "MyStyle");
style.font.color = "#000080";
style.font.name = "Courier New";

expect(style.builtIn).toEqual(false);
```

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

