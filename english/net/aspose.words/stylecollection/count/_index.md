---
title: StyleCollection.Count
linktitle: Count
second_title: Aspose.Words for .NET API Reference
description: StyleCollection Count property. Gets the number of styles in the collection in C#.
type: docs
weight: 10
url: /net/aspose.words/stylecollection/count/
---
## Count property

Gets the number of styles in the collection.

```csharp
public int Count { get; }
```

## Examples

Shows how to add a Style to a document's styles collection.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Set default parameters for new styles that we may later add to this collection.
styles.DefaultFont.Name = "Courier New";
// If we add a style of the "StyleType.Paragraph", the collection will apply the values of
// its "DefaultParagraphFormat" property to the style's "ParagraphFormat" property.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Add a style, and then verify that it has the default settings.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### See Also

* class [StyleCollection](../)
* namespace [Aspose.Words](../../stylecollection/)
* assembly [Aspose.Words](../../../)
