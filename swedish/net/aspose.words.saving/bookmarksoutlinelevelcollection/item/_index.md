---
title: BookmarksOutlineLevelCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Hantera dina bokmärken enkelt med BookmarksOutlineLevelCollection. Ställ in och hämta dispositionsnivåer efter bokmärkesnamn för sömlös organisation.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/bookmarksoutlinelevelcollection/item/
---
## BookmarksOutlineLevelCollection indexer (1 of 2)

Hämtar eller anger en bokmärkesnivå efter bokmärkesnamnet.

```csharp
public int this[string name] { get; set; }
```

| Parameter | Beskrivning |
| --- | --- |
| name | Bokmärkets namn är inte skiftlägeskänsligt. |

### Returvärde

Bokmärkets dispositionsnivå. Giltigt intervall är 0 till 9.

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

* class [BookmarksOutlineLevelCollection](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## BookmarksOutlineLevelCollection indexer (2 of 2)

Hämtar eller ställer in en bokmärkesnivå vid det angivna indexet.

```csharp
public int this[int index] { get; set; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för bokmärket. |

### Returvärde

Bokmärkets dispositionsnivå. Giltigt intervall är 0 till 9.

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

* class [BookmarksOutlineLevelCollection](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
