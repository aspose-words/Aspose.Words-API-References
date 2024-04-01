---
title: ParagraphFormat.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words for .NET
description: ParagraphFormat Style property. Gets or sets the paragraph style applied to this formatting in C#.
type: docs
weight: 350
url: /net/aspose.words/paragraphformat/style/
---
## ParagraphFormat.Style property

Gets or sets the paragraph style applied to this formatting.

```csharp
public Style Style { get; set; }
```

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

### See Also

* class [Style](../../style/)
* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
