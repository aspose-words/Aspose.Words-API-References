---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Få enkelt åtkomst till specifika stycken med egenskapen ParagraphCollection Item. Hämta valfritt stycke via index för smidig texthantering.
type: docs
weight: 10
url: /sv/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

Hämtar en[`Paragraph`](../../paragraph/) vid det givna indexet.

```csharp
public Paragraph this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Ett index till samlingen. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst före sista och så vidare.

Om index är större än eller lika med antalet objekt i listan returnerar detta en nullreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan returnerar detta en null-referens.

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

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
