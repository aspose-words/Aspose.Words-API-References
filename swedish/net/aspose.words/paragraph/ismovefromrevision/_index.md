---
title: Paragraph.IsMoveFromRevision
second_title: Aspose.Words för .NET API Referens
description: Paragraph fast egendom. ReturnerarSann om det här objektet flyttades borttogs i Microsoft Word medan ändringsspårning var aktiverad.
type: docs
weight: 130
url: /sv/net/aspose.words/paragraph/ismovefromrevision/
---
## Paragraph.IsMoveFromRevision property

Returnerar`Sann` om det här objektet flyttades (borttogs) i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsMoveFromRevision { get; }
```

### Exempel

Visar hur man kontrollerar om ett stycke är en flyttversion.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Det här dokumentet innehåller "Move"-versioner, som visas när vi markerar text med markören,
// och sedan dra den för att flytta den till en annan plats
// medan du spårar revisioner i Microsoft Word via "Review" -> "Spåra ändringar".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Flytta revisioner består av par av "Flytta från" och "Flytta till" versioner.
// Dessa ändringar är potentiella ändringar av dokumentet som vi antingen kan acceptera eller förkasta.
// Innan vi accepterar/avvisar en flyttrevision, dokumentet
// måste hålla reda på både avgångs- och ankomstdestinationerna för texten.
// Andra och fjärde stycket definierar en sådan revidering, och båda har alltså samma innehåll.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Revisionen "Flytta från" är stycket där vi drog texten från.
// Om vi accepterar revideringen kommer denna paragraf att försvinna,
// och den andra kommer att finnas kvar och inte längre vara en revision.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Revisionen "Flytta till" är stycket dit vi drog texten till.
// Om vi förkastar revisionen försvinner istället denna paragraf, och den andra kommer att finnas kvar.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../paragraph/)
* hopsättning [Aspose.Words](../../../)


