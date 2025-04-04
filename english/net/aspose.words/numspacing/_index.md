---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.NumSpacing enum to customize numeral spacing for enhanced document formatting. Elevate your text presentation today!
type: docs
weight: 5020
url: /net/aspose.words/numspacing/
---
## NumSpacing enumeration

Specifies possible values in which numeral spacing can be displayed.

```csharp
public enum NumSpacing
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Default | `0` | Specifies that numerals are displayed in the font’s default form. |
| Proportional | `1` | Specifies that the forms of the numerals designed as proportionally spaced are displayed if supported by the font. |
| Tabular | `2` | Specifies that the forms of the numerals designed as tabular are displayed if supported by the font. |

## Examples

Shows how to set the spacing type of the numeral.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// This effect is only supported in newer versions of MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
