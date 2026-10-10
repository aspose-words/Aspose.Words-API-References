---
title: "Aspose::Words::Fields::FieldIndex::get_UseYomi‑metod"
linktitle: "get_UseYomi"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIndex::get_UseYomi metod. Hämtar eller anger huruvida användning av yomi‑text för indexposter ska aktiveras i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.fields/fieldindex/get_useyomi/
---
## FieldIndex::get_UseYomi method


Hämtar eller anger om användning av yomi‑text för indexposter ska aktiveras.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_UseYomi()
```


## Exempel



Visar hur man sorterar INDEX-fältposter fonetiskt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
// och sidnumret som innehåller XE-fältet på höger sida.
// INDEX-posten kommer att samla alla XE-fält med matchande värden i egenskapen "Text".
// till en post istället för att skapa en post för varje XE-fält.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// INDEX-tabellen sorterar automatiskt sina poster efter värdena i deras Text-egenskaper i alfabetisk ordning.
// Ställ in INDEX-tabellen så att den sorterar poster fonetiskt med Hiragana istället.
index->set_UseYomi(sortEntriesUsingYomi);

if (sortEntriesUsingYomi)
{
    ASSERT_EQ(u" INDEX  \\y", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX ", index->GetFieldCode());
}

// Infoga 4 XE-fält, som skulle visas som poster i INDEX-fältets innehållsförteckning.
// "Text"-egenskapen kan innehålla ett ords stavning i Kanji, vars uttal kan vara tvetydigt,
// medan "Yomi"-versionen av ordet exakt visar hur det uttalas med Hiragana.
// Om vi ställer in vårt INDEX-fält att använda Yomi, kommer det att sortera dessa poster
// efter värdet i deras Yomi-egenskaper, istället för deras Text-värden.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛子");
indexEntry->set_Yomi(u"あ");

ASSERT_EQ(u" XE  愛子 \\y あ", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"明美");
indexEntry->set_Yomi(u"あ");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"恵美");
indexEntry->set_Yomi(u"え");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"愛美");
indexEntry->set_Yomi(u"え");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Yomi.docx");
```

## Se även

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
