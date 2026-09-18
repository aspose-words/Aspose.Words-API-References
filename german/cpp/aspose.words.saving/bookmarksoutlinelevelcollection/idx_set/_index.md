---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::idx_set-Methode"
linktitle: "idx_set"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::idx_set-Methode. Ermittelt oder setzt einen Lesezeichen-Gliederungsgrad anhand des Lesezeichennamens in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/idx_set/
---
## BookmarksOutlineLevelCollection::idx_set(const System::String\&, int32_t) method


Liest oder setzt die Gliederungsebene eines Lesezeichens anhand des Lesezeichennamens.

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::idx_set(const System::String &name, int32_t value)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Groß-/Kleinschreibungsunabhängiger Name des Lesezeichens. |

### ReturnValue

Die Gliederungsebene des Lesezeichens. Gültiger Bereich ist 0 bis 9.

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

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## BookmarksOutlineLevelCollection::idx_set(int32_t, int32_t) method


Liest oder setzt die Gliederungsebene eines Lesezeichens am angegebenen Index.

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::idx_set(int32_t index, int32_t value)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Nullbasierter Index des Lesezeichens. |

### ReturnValue

Die Gliederungsebene des Lesezeichens. Gültiger Bereich ist 0 bis 9.

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

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
