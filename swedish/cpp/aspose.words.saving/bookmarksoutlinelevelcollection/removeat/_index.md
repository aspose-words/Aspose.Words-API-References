---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt method. Tar bort ett bokmärke på det angivna indexet i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/removeat/
---
## BookmarksOutlineLevelCollection::RemoveAt method


Tar bort ett bokmärke på det angivna indexet.

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Det nollbaserade indexet. |

## Exempel



Visar hur man ställer in konturnivåer för bokmärken.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett bokmärke med ett annat bokmärke inbäddat i det.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// Infoga ett annat bokmärke.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// När du sparar till .pdf kan bokmärken nås via en rullgardinsmeny och användas som ankare av de flesta läsare.
// Bokmärken kan också ha numeriska värden för konturnivåer,
// vilket möjliggör att lägre nivåns konturposter döljer högre nivåns underposter när de fälls ihop i läsaren.
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// Vi kan ta bort två element så att endast konturnivåbeteckningen för "Bookmark 1" återstår.
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// Det finns nio konturnivåer. Deras numrering kommer att optimeras under sparningsoperationen.
// I detta fall kommer nivåerna "5" och "9" att bli "2" och "3".
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Att tömma denna samling kommer att bevara bokmärkena och placera dem alla på samma konturnivå.
outlineLevels->Clear();
```

## Se även

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
