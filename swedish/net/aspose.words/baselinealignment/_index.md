---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.BaselineAlignment-uppräkningen för exakt teckensnittspositionering. Förbättra din dokumentformatering med optimala vertikala justeringsalternativ.
type: docs
weight: 130
url: /sv/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Anger teckensnittens vertikala position på en rad.

```csharp
public enum BaselineAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Top | `0` | Justerar längs toppen av varje teckensnitt. |
| Center | `1` | Justerar mittpunkterna för varje teckensnitt. |
| Baseline | `2` | Justerar mot styckets baslinje. |
| Bottom | `3` | Justerar längst ner i varje teckensnitt. |
| Auto | `4` | Baslinjen justeras automatiskt. |

## Exempel

Visar hur man ställer in teckensnittens vertikala position på en rad.

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
