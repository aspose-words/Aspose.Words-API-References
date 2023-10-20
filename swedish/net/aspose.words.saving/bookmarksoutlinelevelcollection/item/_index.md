---
title: BookmarksOutlineLevelCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: BookmarksOutlineLevelCollection Item fast egendom. Hämtar eller ställer in en bokmärkeskonturnivå med bokmärkets namn i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/bookmarksoutlinelevelcollection/item/
---
## BookmarksOutlineLevelCollection indexer (1 of 2)

Hämtar eller ställer in en bokmärkeskonturnivå med bokmärkets namn.

```csharp
public int this[string name] { get; set; }
```

| Parameter | Beskrivning |
| --- | --- |
| name | Bokmärkets namn är skiftlägeskänsligt. |

### Returvärde

Konturnivån för bokmärket. Giltigt intervall är 0 till 9.

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

* class [BookmarksOutlineLevelCollection](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## BookmarksOutlineLevelCollection indexer (2 of 2)

Hämtar eller ställer in en bokmärkeskonturnivå vid angivet index.

```csharp
public int this[int index] { get; set; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för bokmärket. |

### Returvärde

Konturnivån för bokmärket. Giltigt intervall är 0 till 9.

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

* class [BookmarksOutlineLevelCollection](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
