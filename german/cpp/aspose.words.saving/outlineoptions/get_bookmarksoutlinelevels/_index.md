---
title: "Aspose::Words::Saving::OutlineOptions::get_BookmarksOutlineLevels Methode"
linktitle: "get_BookmarksOutlineLevels"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::OutlineOptions::get_BookmarksOutlineLevels Methode. Ermöglicht das Festlegen des Gliederungslevels einzelner Lesezeichen in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.saving/outlineoptions/get_bookmarksoutlinelevels/
---
## OutlineOptions::get_BookmarksOutlineLevels method


Ermöglicht das Festlegen der Gliederungsebene einzelner Lesezeichen.

```cpp
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> Aspose::Words::Saving::OutlineOptions::get_BookmarksOutlineLevels() const
```

## Hinweise


Wenn das Lesezeichenlevel in dieser Sammlung nicht angegeben ist, wird der Wert [DefaultBookmarksOutlineLevel](../get_defaultbookmarksoutlinelevel/) verwendet.

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

* Class [BookmarksOutlineLevelCollection](../../bookmarksoutlinelevelcollection/)
* Class [OutlineOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
