---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words för .NET
description: Upptäck LayoutOptions ContinuousSectionPageNumberingRestart-egenskapen för sömlös sidnumreringskontroll i kontinuerliga avsnitt. Optimera din dokumentlayout idag!
type: docs
weight: 40
url: /sv/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Hämtar eller ställer in beteendet för att beräkna sidnummer när ett kontinuerligt avsnitt startar om sidnumreringen.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Anmärkningar

Standardvärdet ärAlways . Det matchar beteendet hos MS Word 2019, som var den senaste versionen när alternativet introducerades. Äldre sidnumreringslogik som demonstrerats av MS Word 2016 är tillgänglig via det här alternativet. Vänligen[`ContinuousSectionRestart`](../../continuoussectionrestart/) för beteendebeskrivningen.

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

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
