---
title: Style.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for NodeJs
description: "Style.remove method. Removes the specified style from the document."
type: docs
weight: 240
url: /nodejs-net/Aspose.Words/style/remove/
---

## remove() {#default}

Removes the specified style from the document.


```js
remove()
```

### Remarks

Style removal has following effects on the document model:

* All references to the style are removed from corresponding paragraphs, runs and tables.
  
* If base style is removed its formatting is moved to child styles.
  
* If style to be deleted has a linked style, then both of these are deleted.
  



### Examples

Shows how to create and apply a custom style.

```js
let doc = new aw.Document();

let style = doc.styles.add(aw.StyleType.Paragraph, "MyStyle");
style.font.name = "Times New Roman";
style.font.size = 16;
style.font.color = "#000080";
// Automatically redefine style.
style.automaticallyUpdate = true;

let builder = new aw.DocumentBuilder(doc);

// Apply one of the styles from the document to the paragraph that the document builder is creating.
builder.paragraphFormat.style = doc.styles.at("MyStyle");
builder.writeln("Hello world!");

let firstParagraphStyle = doc.firstSection.body.firstParagraph.paragraphFormat.style;

expect(firstParagraphStyle).toEqual(style);

// Remove our custom style from the document's styles collection.
doc.styles.at("MyStyle").remove();

firstParagraphStyle = doc.firstSection.body.firstParagraph.paragraphFormat.style;

// Any text that used a removed style reverts to the default formatting.
expect([...doc.styles].every(s => s.name == "MyStyle")).toEqual(false);
expect(firstParagraphStyle.font.name).toEqual("Times New Roman");
expect(firstParagraphStyle.font.size).toEqual(12.0);
expect(firstParagraphStyle.font.color).toEqual(base.emptyColor);
```

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

