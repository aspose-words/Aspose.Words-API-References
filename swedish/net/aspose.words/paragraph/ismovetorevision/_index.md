---
title: Paragraph.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IsMoveToRevision i Microsoft Word! Lär dig hur den spårar ändringar och förbättrar din dokumentredigeringsupplevelse.
type: docs
weight: 140
url: /sv/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

Returer`sann` om det här objektet flyttades (infogades) i Microsoft Word medan ändringsspårning var aktiverad.

```csharp
public bool IsMoveToRevision { get; }
```

## Exempel

Visar hur man kontrollerar om ett stycke är en flyttad revision.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Detta dokument innehåller "Flytta"-revideringar, som visas när vi markerar text med markören,
// och dra den sedan för att flytta den till en annan plats
// vid spårning av revisioner i Microsoft Word via "Granska" -> "Spåra ändringar".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Flyttade revisioner består av par av "Flytta från" och "Flytta till" revisioner.
// Dessa revideringar är potentiella ändringar i dokumentet som vi antingen kan acceptera eller avvisa.
// Innan vi accepterar/avvisar en flyttrevision, dokumentet
// måste hålla reda på både avgångs- och ankomstdestinationer för texten.
// Det andra och fjärde stycket definierar en sådan revision, och har således båda samma innehåll.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Revisionen "Flytta från" är stycket där vi drog texten från.
// Om vi accepterar revisionen kommer detta stycke att försvinna,
// och den andra kommer att finnas kvar och inte längre vara en revision.
Assert.True(paragraphs[1].IsMoveFromRevision);

// "Flytta till"-versionen är stycket dit vi drog texten.
// Om vi avvisar revisionen kommer istället detta stycke att försvinna, och det andra kommer att finnas kvar.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Se även

* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
