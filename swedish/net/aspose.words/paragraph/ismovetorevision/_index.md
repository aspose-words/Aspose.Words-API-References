---
title: Paragraph.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words för .NET
description: Paragraph IsMoveToRevision fast egendom. ReturnerarSann om detta objekt flyttades infogades i Microsoft Word medan ändringsspårning var aktiverad i C#.
type: docs
weight: 140
url: /sv/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

Returnerar`Sann` om detta objekt flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsMoveToRevision { get; }
```

## Exempel

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
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
