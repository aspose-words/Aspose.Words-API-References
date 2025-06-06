---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Underline enum for versatile font underlining options. Enhance your document formatting with customizable styles today!
type: docs
weight: 7370
url: /net/aspose.words/underline/
---
## Underline enumeration

Indicates type of the underline applied to a font.

```csharp
public enum Underline
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

## Examples

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
