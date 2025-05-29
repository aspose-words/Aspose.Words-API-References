---
title: ParagraphCollection Class
linktitle: ParagraphCollection
articleTitle: ParagraphCollection
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.ParagraphCollection för sömlös åtkomst till strukturerade styckenoder, vilket förbättrar dokumenthantering och effektivitet i dina projekt.
type: docs
weight: 5140
url: /sv/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Ger maskinskriven åtkomst till en samling av[`Paragraph`](../paragraph/) noder.

För att lära dig mer, besök[Arbeta med stycken](https://docs.aspose.com/words/net/working-with-paragraphs/) dokumentationsartikel.

```csharp
public class ParagraphCollection : NodeCollection
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Hämtar antalet noder i samlingen. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Hämtar en[`Paragraph`](../paragraph/) vid det givna indexet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från den här samlingen och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Avgör om en nod finns i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Ger en enkel iteration i "foreach"-stil över samlingen av noder. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Infogar en nod i samlingen vid det angivna indexet. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Tar bort noden vid det angivna indexet från samlingen och från dokumentet. |
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Kopierar alla stycken från samlingen till en ny matris med stycken. (2 methods) |

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

* class [NodeCollection](../nodecollection/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
