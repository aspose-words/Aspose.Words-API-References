---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words för .NET
description: Aspose.Words.Layout.ContinuousSectionRestart uppräkning. Representerar olika beteenden vid beräkning av sidnummer i ett kontinuerligt avsnitt som startar om sidnumreringen i C#.
type: docs
weight: 3300
url: /sv/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Representerar olika beteenden vid beräkning av sidnummer i ett kontinuerligt avsnitt som startar om sidnumreringen.

```csharp
public enum ContinuousSectionRestart
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Always | `0` | Sidnumrering startar alltid om oavsett innehållsflöde. |
| FromNewPageOnly | `1` | Sidnumrering startar om endast om det inte finns något annat innehåll före avsnittet på sidan där avsnittet börjar. |

## Exempel

Visar hur man styr sidnumreringen i ett kontinuerligt avsnitt.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Som standard matchar Aspose.Words-beteendet Microsoft Word 2019.
// Om du behöver gammalt beteende från Aspose.Words, upprepande Microsoft Word 2016, använd 'ContinuousSectionRestart.FromNewPageOnly'.
// Sidnumrering startar om endast om det inte finns något annat innehåll före avsnittet på sidan där avsnittet börjar,
// på grund av det kommer numreringen att återställas till 2 från den andra sidan.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
