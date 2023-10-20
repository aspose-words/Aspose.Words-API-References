---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words för .NET
description: Aspose.Words.BaselineAlignment uppräkning. Anger teckensnittens vertikala position på en linje i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Anger teckensnittens vertikala position på en linje.

```csharp
public enum BaselineAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Top | `0` | Justeras längst upp på varje teckensnitt. |
| Center | `1` | Justerar mittpunkterna för varje teckensnitt. |
| Baseline | `2` | Justeras till styckets baslinje. |
| Bottom | `3` | Justeras till botten av varje teckensnitt. |
| Auto | `4` | Baslinjen justeras automatiskt. |

## Exempel

Visar hur du ställer in teckensnitt vertikalt på en linje.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
