---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: ParagraphCollection Item fast egendom. Hämtar enParagraph vid det givna indexet i C#.
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
| index | Ett index i samlingen. |

## Anmärkningar

Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från baksidan av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder näst före sist och så vidare.

Om index är större än eller lika med antalet objekt i listan, returnerar detta en nollreferens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan, returnerar detta en nollreferens.

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

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
