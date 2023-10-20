---
title: BookmarksOutlineLevelCollection Class
linktitle: BookmarksOutlineLevelCollection
articleTitle: BookmarksOutlineLevelCollection
second_title: Aspose.Words för .NET
description: Aspose.Words.Saving.BookmarksOutlineLevelCollection klass. En samling individuella bokmärken konturnivå i C#.
type: docs
weight: 4850
url: /sv/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

En samling individuella bokmärken konturnivå.

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
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Hämtar eller ställer in en bokmärkeskonturnivå med bokmärkets namn. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(*string, int*) | Lägger till ett bokmärke i samlingen. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Tar bort alla element från samlingen. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(*string*) | Bestämmer om samlingen innehåller ett bokmärke med det angivna namnet. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(*string*) | Returnerar det nollbaserade indexet för det angivna bokmärket i samlingen. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(*string*) | Tar bort ett bokmärke med det angivna namnet från samlingen. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(*int*) | Tar bort ett bokmärke vid det angivna indexet. |

## Anmärkningar

Nyckel är ett bokmärkesnamn för strängar som inte är skiftlägeskänsliga. Värde är en int bokmärkeskonturnivå.

Bokmärkeskonturnivå kan vara ett värde från 0 till 9. Ange 0 och Word-bokmärke kommer inte att visas i dokumentkonturen. Ange 1 och Word-bokmärke kommer att visas i dokumentkonturen på nivå 1; 2 för nivå 2 och så vidare.

## Exempel

Visar hur du ställer in konturnivåer för bokmärken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett bokmärke med ett annat bokmärke kapslat inuti.
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

// När du sparar till .pdf kan bokmärken nås via en rullgardinsmeny och användas som ankare av de flesta läsare.
// Bokmärken kan också ha numeriska värden för konturnivåer,
// möjliggör för konturposter på lägre nivå att dölja underordnade poster på högre nivå när de komprimeras i läsaren.
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

// Vi kan ta bort två element så att endast konturnivåbeteckningen för "Bokmärke 1" finns kvar.
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Det finns nio konturnivåer. Deras numrering kommer att optimeras under lagringsoperationen.
// I det här fallet kommer nivåerna "5" och "9" att bli "2" och "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Att tömma den här samlingen kommer att bevara bokmärkena och placera dem alla på samma konturnivå.
outlineLevels.Clear();
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
