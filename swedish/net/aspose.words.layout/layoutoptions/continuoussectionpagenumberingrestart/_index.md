---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
second_title: Aspose.Words för .NET API Referens
description: LayoutOptions fast egendom. Hämtar eller ställer in beteendet för beräkning av sidnummer när ett kontinuerligt avsnitt startar om sidnumreringen.
type: docs
weight: 40
url: /sv/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Hämtar eller ställer in beteendet för beräkning av sidnummer när ett kontinuerligt avsnitt startar om sidnumreringen.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

### Anmärkningar

Standardvärdet ärAlways. Det matchar beteendet hos MS Word 2019 som var den senaste versionen vid det ögonblick då alternativet introducerades. Äldre sidnumreringslogik som demonstreras av MS Word 2016 är tillgänglig via detta alternativ. Vänligen[`ContinuousSectionRestart`](../../continuoussectionrestart/) för beteendebeskrivningen.

### Exempel

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

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../layoutoptions/)
* hopsättning [Aspose.Words](../../../)


