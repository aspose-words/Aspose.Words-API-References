---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection klass"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection klass. En samling av individuella bokmärkenas konturnivå. Läs mer genom att besöka dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class


En samling av individuella bokmärken på kontur‑nivå. För att lära dig mer, besök dokumentationsartikeln [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarksOutlineLevelCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, int32_t>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::String\&, int32_t) | Lägger till ett bokmärke i samlingen. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/)() |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Tar bort alla element från samlingen. |
| [Contains](./contains/)(const System::String\&) | Bestämmer om samlingen innehåller ett bokmärke med det angivna namnet. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Hämtar eller sätter en bokmärkeskonturnivå efter bokmärkesnamnet. |
| [idx_get](./idx_get/)(int32_t) | Hämtar eller sätter en bokmärkeskonturnivå på det angivna indexet. |
| [idx_set](./idx_set/)(const System::String\&, int32_t) | Hämtar eller sätter en bokmärkeskonturnivå efter bokmärkesnamnet. |
| [idx_set](./idx_set/)(int32_t, int32_t) | Hämtar eller sätter en bokmärkeskonturnivå på det angivna indexet. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Returnerar det nollbaserade indexet för den angivna bokmärket i samlingen. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Tar bort ett bokmärke med det angivna namnet från samlingen. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort ett bokmärke på det angivna indexet. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beskrivning |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Anmärkningar


Nyckel är ett skiftlägesokänsligt strängnamn för bokmärke. Värde är ett heltal som anger bokmärkets konturnivå.

[Bookmark](../../aspose.words/bookmark/) outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
