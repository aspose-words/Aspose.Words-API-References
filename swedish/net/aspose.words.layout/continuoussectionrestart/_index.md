---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.Layout.ContinuousSectionRestart-uppräkningen för flexibla sidnumreringsalternativ i kontinuerliga avsnitt. Förbättra dokumentlayouten utan ansträngning!
type: docs
weight: 3750
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
| Always | `0` | Sidnumreringen startar alltid om oavsett innehållsflöde. |
| FromNewPageOnly | `1` | Sidnumreringen startar bara om om det inte finns något annat innehåll före avsnittet på sidan där avsnittet börjar. |

## Exempel

Visar hur man styr sidnumreringen i ett kontinuerligt avsnitt.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Som standard matchar Aspose.Words beteende Microsoft Word 2019.
// Om du behöver gammalt Aspose.Words-beteende, repetitivt Microsoft Word 2016, använd 'ContinuousSectionRestart.FromNewPageOnly'.
// Sidnumreringen startar bara om om det inte finns något annat innehåll före avsnittet på sidan där avsnittet börjar,
// på grund av det återställs numreringen till 2 från och med den andra sidan.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
