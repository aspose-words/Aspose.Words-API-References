---
title: Style.automaticallyUpdate property
linktitle: automaticallyUpdate property
articleTitle: automaticallyUpdate property
second_title: Aspose.Words for Node.js
description: "Style.automaticallyUpdate property. Specifies whether this style is automatically redefined based on the appropriate value."
type: docs
weight: 20
url: /nodejs-net/aspose.words/style/automaticallyUpdate/
---

## Style.automaticallyUpdate property

Specifies whether this style is automatically redefined based on the appropriate value.


```js
get automaticallyUpdate(): boolean
```

### Remarks

If the property value is set to true, MS Word automatically redefines the current style when
the appropriate paragraph formatting has been changed.

AutomaticallyUpdate property is applicable to paragraph styles only.

The default value is ``false``.




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

