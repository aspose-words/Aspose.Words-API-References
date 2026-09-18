---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection Klasse"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection Klasse. Eine Sammlung von einzelnen Lesezeichen-Gliederungsebenen. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class


Eine Sammlung von einzelnen Lesezeichen-Gliederungsebenen. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarksOutlineLevelCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, int32_t>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::String\&, int32_t) | Fügt ein Lesezeichen zur Sammlung hinzu. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/)() |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Contains](./contains/)(const System::String\&) | Bestimmt, ob die Sammlung ein Lesezeichen mit dem angegebenen Namen enthält. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Liest oder setzt die Gliederungsebene eines Lesezeichens anhand des Lesezeichennamens. |
| [idx_get](./idx_get/)(int32_t) | Liest oder setzt die Gliederungsebene eines Lesezeichens am angegebenen Index. |
| [idx_set](./idx_set/)(const System::String\&, int32_t) | Liest oder setzt die Gliederungsebene eines Lesezeichens anhand des Lesezeichennamens. |
| [idx_set](./idx_set/)(int32_t, int32_t) | Liest oder setzt die Gliederungsebene eines Lesezeichens am angegebenen Index. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Gibt den nullbasierten Index des angegebenen Lesezeichens in der Sammlung zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Entfernt ein Lesezeichen mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt ein Lesezeichen am angegebenen Index. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Hinweise


Der Schlüssel ist ein schreibweiseunabhängiger Zeichenketten-Lesezeichenname. Der Wert ist ein int Lesezeichen-Gliederungslevel.

[Bookmark](../../aspose.words/bookmark/) outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.

## Beispiele



Zeigt, wie Gliederungsebenen für Lesezeichen festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt ein Lesezeichen ein, in dem ein weiteres Lesezeichen verschachtelt ist.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// Fügt ein weiteres Lesezeichen ein.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// Beim Speichern als .pdf können Lesezeichen über ein Dropdown-Menü aufgerufen und von den meisten Lesern als Anker verwendet werden.
// Lesezeichen können auch numerische Werte für Gliederungsebenen haben,
// ermöglicht es, dass niedrigere Gliederungseinträge höhere Kindeinträge ausblenden, wenn sie im Reader zusammengeklappt werden.
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

// Wir können zwei Elemente entfernen, sodass nur die Gliederungsebene‑Bezeichnung für "Bookmark 1" übrig bleibt.
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// Es gibt neun Gliederungsebenen. Ihre Nummerierung wird während des Speicher‑Vorgangs optimiert.
// In diesem Fall werden die Ebenen "5" und "9" zu "2" und "3".
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Das Leeren dieser Sammlung bewahrt die Lesezeichen und legt sie alle auf dieselbe Gliederungsebene.
outlineLevels->Clear();
```

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
