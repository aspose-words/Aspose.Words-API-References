---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words for .NET
description: Discover the Font Bold property: easily identify if your text is bolded, enhancing readability and style for your web design projects.
type: docs
weight: 40
url: /net/aspose.words/font/bold/
---
## Font.Bold property

True if the font is formatted as bold.

```csharp
public bool Bold { get; set; }
```

## Examples

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

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
