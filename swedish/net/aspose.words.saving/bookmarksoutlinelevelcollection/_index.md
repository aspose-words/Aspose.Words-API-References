---
title: BookmarksOutlineLevelCollection Class
linktitle: BookmarksOutlineLevelCollection
articleTitle: BookmarksOutlineLevelCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.BookmarksOutlineLevelCollection – ett kraftfullt verktyg för att hantera bokmärken och förbättra dokumentnavigering utan ansträngning.
type: docs
weight: 5590
url: /sv/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

En samling individuella bokmärken på dispositionsnivå.

För att lära dig mer, besök[Arbeta med bokmärken](https://docs.aspose.com/words/net/working-with-bookmarks/) dokumentationsartikel.

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Hämtar eller anger en bokmärkesnivå efter bokmärkesnamnet. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(*string, int*) | Lägger till ett bokmärke i samlingen. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Tar bort alla element från samlingen. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(*string*) | Avgör om samlingen innehåller ett bokmärke med det angivna namnet. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | Returnerar ett uppräknarobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(*string*) | Returnerar det nollbaserade indexet för det angivna bokmärket i samlingen. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(*string*) | Tar bort ett bokmärke med det angivna namnet från samlingen. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(*int*) | Tar bort ett bokmärke vid det angivna indexet. |

## Anmärkningar

Key är ett skiftläges-okänsligt bokmärkesnamn. Value är ett heltal på bokmärkets dispositionsnivå.

Bokmärkesdispositionens nivå kan vara ett värde från 0 till 9. Ange 0 så visas inte Word-bokmärket i dokumentdispositionen. Ange 1 så visas Word-bokmärket i dokumentdispositionen på nivå 1; 2 för nivå 2 och så vidare.

## Exempel

Visar hur man ställer in konturnivåer för bokmärken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett bokmärke med ett annat bokmärke inbäddat inuti det.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Infoga ett annat bokmärke.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// När man sparar till .pdf kan bokmärken nås via en rullgardinsmeny och användas som ankare av de flesta läsare.
// Bokmärken kan också ha numeriska värden för dispositionsnivåer,
// aktiverar dispositionsposter på lägre nivå för att dölja underordnade poster på högre nivå när de är hopfällda i läsaren.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// Vi kan ta bort två element så att endast beteckningen för dispositionsnivå för "Bokmärke 1" finns kvar.
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Det finns nio dispositionsnivåer. Numreringen av dem optimeras när de sparas.
// I det här fallet blir nivåerna "5" och "9" "2" och "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Om du tömmer den här samlingen bevaras bokmärkena och de placeras alla på samma dispositionsnivå.
outlineLevels.Clear();
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
