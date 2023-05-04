---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words for .NET
description: Style AutomaticallyUpdate property. Specifies whether this style is automatically redefined based on the appropriate value in C#.
type: docs
weight: 20
url: /net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Specifies whether this style is automatically redefined based on the appropriate value.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Remarks

If the property value is set to true, MS Word automatically redefines the current style when the appropriate paragraph formatting has been changed.

AutomaticallyUpdate property is applicable to paragraph styles only.

The default value is `false`.

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
* namespace [Aspose.Words](../../style/)
* assembly [Aspose.Words](../../../)
