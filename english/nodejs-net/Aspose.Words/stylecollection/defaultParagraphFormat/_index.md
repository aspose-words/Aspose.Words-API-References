---
title: StyleCollection.defaultParagraphFormat property
linktitle: defaultParagraphFormat property
articleTitle: defaultParagraphFormat property
second_title: Aspose.Words for NodeJs
description: "StyleCollection.defaultParagraphFormat property. Gets document default paragraph formatting."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words/stylecollection/defaultParagraphFormat/
---

## StyleCollection.defaultParagraphFormat property

Gets document default paragraph formatting.


```js
get defaultParagraphFormat(): Aspose.Words.ParagraphFormat
```

### Remarks

Note that document-wide defaults were introduced in Microsoft Word 2007 and are fully supported in OOXML formats ([LoadFormat.Docx](../../loadformat/#Docx)) only.
Earlier document formats have no support for document default paragraph formatting.




### Examples

Shows how to add a Style to a document's styles collection.

```js
let doc = new aw.Document();

let styles = doc.styles;
// Set default parameters for new styles that we may later add to this collection.
styles.defaultFont.name = "Courier New";
// If we add a style of the "StyleType.Paragraph", the collection will apply the values of
// its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
styles.defaultParagraphFormat.firstLineIndent = 15.0;
// Add a style, and then verify that it has the default settings.
styles.add(aw.StyleType.Paragraph, "MyStyle");

expect(styles.at(4).font.name).toEqual("Courier New");
expect(styles.at("MyStyle").paragraphFormat.firstLineIndent).toEqual(15.0);
```

### See Also

* module [Aspose.Words](../../)
* class [StyleCollection](../)

