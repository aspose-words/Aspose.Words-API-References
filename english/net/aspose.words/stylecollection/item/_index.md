---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Discover StyleCollection's powerful Item property to effortlessly retrieve styles by name or alias, enhancing your design experience with ease!
type: docs
weight: 50
url: /net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Gets a style by name or alias.

```csharp
public Style this[string name] { get; }
```

## Remarks

Case sensitive, returns `null` if the style with the given name is not found.

If this is an English name of a built in style that does not yet exist, automatically creates it.

## Examples

Shows when to recalculate the page layout of the document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Saving a document to PDF, to an image, or printing for the first time will automatically
// cache the layout of the document within its pages.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modify the document in some way.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// In the current version of Aspose.Words, modifying the document does not automatically rebuild
// the cached page layout. If we wish for the cached layout
// to stay up to date, we will need to update it manually.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### See Also

* class [Style](../../style/)
* class [StyleCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Gets a built-in style by its locale independent identifier.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parameter | Description |
| --- | --- |
| sti | A [`StyleIdentifier`](../../styleidentifier/) value that specifies the built in style to retrieve. |

## Remarks

When accessing a style that does not yet exist, automatically creates it.

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

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Gets a style by index.

```csharp
public Style this[int index] { get; }
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

Assert.That(styles[4].Font.Name, Is.EqualTo("Courier New"));
Assert.That(styles["MyStyle"].ParagraphFormat.FirstLineIndent, Is.EqualTo(15.0));
```

### See Also

* class [Style](../../style/)
* class [StyleCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
