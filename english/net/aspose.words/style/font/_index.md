---
title: Style.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: Discover the Style Font property to enhance your character formatting effortlessly. Unlock unique styling options for a polished look!
type: docs
weight: 60
url: /net/aspose.words/style/font/
---
## Style.Font property

Gets the character formatting of the style.

```csharp
public Font Font { get; }
```

## Remarks

For list styles this property returns `null`.

## Examples

Shows how to create and use a paragraph style with list formatting.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a custom paragraph style.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Create a list and make sure the paragraphs that use this style will use this list.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

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

Assert.That(firstParagraphStyle, Is.EqualTo(style));

// Remove our custom style from the document's styles collection.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Any text that used a removed style reverts to the default formatting.
Assert.That(doc.Styles.Any(s => s.Name == "MyStyle"), Is.False);
Assert.That(firstParagraphStyle.Font.Name, Is.EqualTo("Times New Roman"));
Assert.That(firstParagraphStyle.Font.Size, Is.EqualTo(12.0d));
Assert.That(firstParagraphStyle.Font.Color.ToArgb(), Is.EqualTo(Color.Empty.ToArgb()));
```

### See Also

* class [Font](../../font/)
* class [Style](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
