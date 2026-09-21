---
title: "Aspose::Words::Bookmark::get_Name metod"
linktitle: "get_Name"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Bookmark::get_Name metod. Hämtar eller anger namnet på bokmärket i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


Hämtar eller anger namnet på bokmärket.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Exempel



Visar hur man infogar ett bokmärke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ett giltigt bokmärke har ett namn, en BookmarkStart och en BookmarkEnd‑nod.
// Alla blanksteg i bokmärkens namn kommer att konverteras till understreck om vi öppnar det sparade dokumentet med Microsoft Word.
// Om vi markerar bokmärkets namn i Microsoft Word via Infoga -> Länkar -> Bokmärke och trycker på "Gå till",
// kommer markören att hoppa till texten som omges av BookmarkStart‑ och BookmarkEnd‑noderna.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// Bokmärken lagras i den här samlingen.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## Se även

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
