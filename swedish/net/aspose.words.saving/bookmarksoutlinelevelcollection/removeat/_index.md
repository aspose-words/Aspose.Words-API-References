---
title: BookmarksOutlineLevelCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words för .NET
description: Hantera enkelt dina bokmärken med metoden RemoveAt. Ta snabbt bort bokmärken efter index för en effektivare upplevelse i din applikation!
type: docs
weight: 100
url: /sv/net/aspose.words.saving/bookmarksoutlinelevelcollection/removeat/
---
## BookmarksOutlineLevelCollection.RemoveAt method

Tar bort ett bokmärke vid det angivna indexet.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Det nollbaserade indexet. |

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
