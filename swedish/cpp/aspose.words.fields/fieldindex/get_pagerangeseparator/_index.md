---
title: "Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator method"
linktitle: "get_PageRangeSeparator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator method. Hämtar eller anger teckensekvensen som används för att separera början och slutet av ett sidintervall i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.fields/fieldindex/get_pagerangeseparator/
---
## FieldIndex::get_PageRangeSeparator method


Hämtar eller anger teckensekvensen som används för att separera början och slutet av ett sidintervall.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator()
```


## Exempel



Visar hur man anger ett bokmärkes omfattade sidor som ett sidintervall för en INDEX-fältpost.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
// och sidnumret som innehåller XE-fältet på höger sida.
// INDEX-posten kommer att samla alla XE-fält med matchande värden i egenskapen "Text".
// till en post istället för att skapa en post för varje XE-fält.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// För INDEX-poster som visar sidintervall kan vi ange en avgränsningssträng
// som kommer att visas mellan numret på den första sidan och numret på den sista.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// Om ett XE-fält namnger ett bokmärke med egenskapen PageRangeBookmarkName,
// kommer dess INDEX-post att visa det sidintervall som bokmärket omfattar
// i stället för numret på den sida som innehåller XE-fältet.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// Infoga ett bokmärke som börjar på sida 3 och slutar på sida 5.
// INDEX-posten för XE-fältet som refererar till detta bokmärke kommer att visa detta sidintervall.
// I vår tabell kommer INDEX-posten att visa "My entry, on page(s) 3 to 5".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## Se även

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
