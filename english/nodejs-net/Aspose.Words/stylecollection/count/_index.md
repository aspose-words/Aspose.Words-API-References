---
title: StyleCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for NodeJs
description: "StyleCollection.count property. Gets the number of styles in the collection."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/stylecollection/count/
---

## StyleCollection.count property

Gets the number of styles in the collection.


```js
get count(): number
```

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

