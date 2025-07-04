---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words for .NET
description: Discover the StyleCollection DefaultFont property for seamless document text formatting. Enhance your documents with consistent, professional style.
type: docs
weight: 20
url: /net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

Gets document default text formatting.

```csharp
public Font DefaultFont { get; }
```

## Remarks

Note that document-wide defaults were introduced in Microsoft Word 2007 and are fully supported in OOXML formats (Docx) only. Earlier document formats have limited support for this feature and only font names can be stored.

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

Assert.That(styles[4].Font.Name, Is.EqualTo("Courier New"));
Assert.That(styles["MyStyle"].ParagraphFormat.FirstLineIndent, Is.EqualTo(15.0));
```

### See Also

* class [Font](../../font/)
* class [StyleCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
