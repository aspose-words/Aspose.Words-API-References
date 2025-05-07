---
title: CleanupOptions.duplicateStyle property
linktitle: duplicateStyle property
articleTitle: duplicateStyle property
second_title: Aspose.Words for Node.js
description: "CleanupOptions.duplicateStyle property. Gets/sets a flag indicating whether duplicate styles should be removed from document"
type: docs
weight: 20
url: /nodejs-net/aspose.words/cleanupoptions/duplicateStyle/
---

## CleanupOptions.duplicateStyle property

Gets/sets a flag indicating whether duplicate styles should be removed from document.
Default value is ``false``.



```js
get duplicateStyle(): boolean
```

### Examples

Shows how to remove duplicated styles from the document.

```js
let doc = new aw.Document();

// Add two styles to the document with identical properties,
// but different names. The second style is considered a duplicate of the first.
let myStyle = doc.styles.add(aw.StyleType.Paragraph, "MyStyle1");
myStyle.font.size = 14;
myStyle.font.name = "Courier New";
myStyle.font.color = "blue";

let duplicateStyle = doc.styles.add(aw.StyleType.Paragraph, "MyStyle2");
duplicateStyle.font.size = 14;
duplicateStyle.font.name = "Courier New";
duplicateStyle.font.color = "blue";

expect(doc.styles.count).toEqual(6);

// Apply both styles to different paragraphs within the document.
let builder = new aw.DocumentBuilder(doc);
builder.paragraphFormat.styleName = myStyle.name;
builder.writeln("Hello world!");

builder.paragraphFormat.styleName = duplicateStyle.name;
builder.writeln("Hello again!");

let paragraphs = doc.firstSection.body.paragraphs;

expect(paragraphs.at(0).paragraphFormat.style).toEqual(myStyle);
expect(paragraphs.at(1).paragraphFormat.style).toEqual(duplicateStyle);

// Configure a CleanOptions object, then call the Cleanup method to substitute all duplicate styles
// with the original and remove the duplicates from the document.
let cleanupOptions = new aw.CleanupOptions();
cleanupOptions.duplicateStyle = true;

doc.cleanup(cleanupOptions);

expect(doc.styles.count).toEqual(5);
expect(paragraphs.at(0).paragraphFormat.style).toEqual(myStyle);
expect(paragraphs.at(1).paragraphFormat.style).toEqual(myStyle);
```

### See Also

* module [Aspose.Words](../../)
* class [CleanupOptions](../)

