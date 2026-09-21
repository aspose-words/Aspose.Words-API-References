---
title: "Aspose::Words::Fields::FieldIndex::get_BookmarkName metod"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIndex::get_BookmarkName metod. Hämtar eller anger namnet på bokmärket som markerar den del av dokumentet som används för att bygga indexet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldindex/get_bookmarkname/
---
## FieldIndex::get_BookmarkName method


Hämtar eller anger namnet på bokmärket som markerar den del av dokumentet som används för att bygga indexet.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_BookmarkName()
```


## Exempel



Visar hur man skapar ett INDEX-fält och sedan använder XE-fält för att fylla det med poster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida
// och sidan som innehåller XE-fältet på höger sida.
// Om XE-fälten har samma värde i deras \"Text\"-egenskap,
// kommer INDEX-fältet att gruppera dem till en post.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Konfigurera INDEX-fältet så att det endast visar XE-fält som ligger inom gränserna
// för ett bokmärke med namnet \"MainBookmark\" och vars \"EntryType\"-egenskaper har värdet \"A\".
// För både INDEX- och XE-fält använder \"EntryType\"-egenskapen endast det första tecknet i dess strängvärde.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// På en ny sida, starta bokmärket med ett namn som matchar värdet
// för INDEX-fältets \"BookmarkName\"-egenskap.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// INDEX-fältet kommer att plocka upp den här posten eftersom den ligger inom bokmärket,
// och dess posttyp matchar också INDEX-fältets posttyp.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Infoga ett XE-fält som inte kommer att visas i INDEX eftersom posttyperna inte matchar.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Avsluta bokmärket och infoga ett XE-fält efteråt.
// Det är av samma typ som INDEX-fältet, men kommer inte att visas
// eftersom det är utanför bokmärkets gränser.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```

## Se även

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
