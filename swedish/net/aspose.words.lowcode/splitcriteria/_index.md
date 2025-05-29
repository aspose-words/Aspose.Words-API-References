---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.LowCode.SplitCriteria-enum för effektiv dokumentdelning. Optimera ditt arbetsflöde med mångsidiga alternativ för sömlös delhantering.
type: docs
weight: 4400
url: /sv/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

Anger hur dokumentet delas upp i delar.

```csharp
public enum SplitCriteria
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Page | `0` | Anger att dokumentet är uppdelat i sidor. |
| SectionBreak | `1` | Anger att dokumentet delas upp i delar vid en sektionsbrytning av valfri typ. |
| Style | `2` | Anger att dokumentet delas upp i delar vid ett stycke formaterat med den stil som anges i[`SplitStyle`](../splitoptions/splitstyle/) . |

## Exempel

Visar hur man delar upp dokumentet efter sidor.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Se även

* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
