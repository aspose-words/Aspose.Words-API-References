---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words for .NET API Reference
description: Font Underline property. Gets or sets the type of underline applied to the font in C#.
type: docs
weight: 530
url: /net/aspose.words/font/underline/
---
## Font.Underline property

Gets or sets the type of underline applied to the font.

```csharp
public Underline Underline { get; set; }
```

## Examples

Shows how to configure the style and color of a text underline.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

Shows how to insert formatted text using DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specify font formatting, then add text.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Shows how to insert a hyperlink field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Insert a hyperlink and emphasize it with custom formatting.
// The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### See Also

* enum [Underline](../../underline/)
* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
