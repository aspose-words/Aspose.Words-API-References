---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words for .NET
description: Font TintAndShade property. Gets or sets a double value that lightens or darkens a color in C#.
type: docs
weight: 520
url: /net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Gets or sets a double value that lightens or darkens a color.

```csharp
public double TintAndShade { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentOutOfRangeException | Throw if set this property to a value less than -1 or more than 1. |
| InvalidOperationException | Throw if set this property for [`Font`](../) object with non-theme colors. |

## Remarks

The allowed values are in range from -1 (darkest) to 1 (lightest) for this property.

Zero (0) is neutral.

## Examples

Shows how to create and use themed style.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Create some style with theme font properties.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
