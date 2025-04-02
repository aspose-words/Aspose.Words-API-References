---
title: CleanupOptions.unusedStyles property
linktitle: unusedStyles property
articleTitle: unusedStyles property
second_title: Aspose.Words for NodeJs
description: "CleanupOptions.unusedStyles property. Specifies whether unused styles should be removed from document"
type: docs
weight: 50
url: /nodejs-net/Aspose.Words/cleanupoptions/unusedStyles/
---

## CleanupOptions.unusedStyles property

Specifies whether unused styles should be removed from document.
Default value is ``True``.



```js
get unusedStyles(): boolean
```

### Examples

Shows how to remove all unused custom styles from a document.

```js
let doc = new aw.Document();

doc.styles.add(aw.StyleType.List, "MyListStyle1");
doc.styles.add(aw.StyleType.List, "MyListStyle2");
doc.styles.add(aw.StyleType.Character, "MyParagraphStyle1");
doc.styles.add(aw.StyleType.Character, "MyParagraphStyle2");

// Combined with the built-in styles, the document now has eight styles.
// A custom style is marked as "used" while there is any text within the document
// formatted in that style. This means that the 4 styles we added are currently unused.
expect(doc.styles.count).toEqual(8);

// Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
let builder = new aw.DocumentBuilder(doc);
builder.font.style = doc.styles.at("MyParagraphStyle1");
builder.writeln("Hello world!");

let list = doc.lists.add(doc.styles.at("MyListStyle1"));
builder.listFormat.list = list;
builder.writeln("Item 1");
builder.writeln("Item 2");

// Now, there is one unused character style and one unused list style.
// The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
let cleanupOptions = new aw.CleanupOptions();
cleanupOptions.unusedLists = true;
cleanupOptions.unusedStyles = true;
cleanupOptions.unusedBuiltinStyles = true;

doc.cleanup(cleanupOptions);

expect(doc.styles.count).toEqual(4);

// Removing every node that a custom style is applied to marks it as "unused" again. 
// Rerun the Cleanup method to remove them.
doc.firstSection.body.removeAllChildren();
doc.cleanup(cleanupOptions);

expect(doc.styles.count).toEqual(2);
```

### See Also

* module [Aspose.Words](../../)
* class [CleanupOptions](../)

