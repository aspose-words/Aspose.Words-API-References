---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Effortlessly eliminate unwanted styles from your document with the Style Remove method. Enhance your content's appearance and maintain consistency!
type: docs
weight: 230
url: /net/aspose.words/style/remove/
---
## Style.Remove method

Removes the specified style from the document.

```csharp
public void Remove()
```

## Remarks

Style removal has following effects on the document model:

* All references to the style are removed from corresponding paragraphs, runs and tables.
* If base style is removed its formatting is moved to child styles.
* If style to be deleted has a linked style, then both of these are deleted.

## Examples

Shows how to create and apply a custom style.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Automatically redefine style.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Apply one of the styles from the document to the paragraph that the document builder is creating.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Remove our custom style from the document's styles collection.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Any text that used a removed style reverts to the default formatting.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### See Also

* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
