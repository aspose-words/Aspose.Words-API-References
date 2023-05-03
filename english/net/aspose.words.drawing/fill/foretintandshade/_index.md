---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
second_title: Aspose.Words for .NET API Reference
description: Fill ForeTintAndShade property. Gets or sets a double value that lightens or darkens the foreground color in C#.
type: docs
weight: 70
url: /net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Gets or sets a double value that lightens or darkens the foreground color.

```csharp
public double ForeTintAndShade { get; set; }
```

## Remarks

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in ArgumentOutOfRangeException.

## Examples

Shows how to manage lightening and darkening foreground font color.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../fill/)
* assembly [Aspose.Words](../../../)
