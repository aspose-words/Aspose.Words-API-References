---
title: "Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine metod"
linktitle: "get_RunSubentriesOnSameLine"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine metod. Hämtar eller anger huruvida underposter körs på samma rad som huvudposten i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.fields/fieldindex/get_runsubentriesonsameline/
---
## FieldIndex::get_RunSubentriesOnSameLine method


Hämtar eller anger om underposter ska köras på samma rad som huvudposten.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine()
```


## Exempel



Visar hur man arbetar med underposter i ett INDEX‑fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
// och sidnumret som innehåller XE-fältet på höger sida.
// INDEX-posten kommer att samla alla XE-fält med matchande värden i egenskapen "Text".
// till en post istället för att skapa en post för varje XE-fält.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_PageNumberSeparator(u", see page ");
index->set_Heading(u"A");

// XE‑fält som har en Text‑egenskap vars värde blir rubriken för INDEX‑posten.
// Om detta värde innehåller två strängsegment separerade med ett kolon (INDEX‑posten kommer att behandla :) som avgränsare,
// det första segmentet är rubrik, och det andra segmentet blir underrubrik.
// INDEX‑fältet grupperar först poster alfabetiskt, och sedan, om det finns flera XE‑fält med samma
// rubriker, kommer INDEX‑fältet att ytterligare undergruppera dem efter värdena för dessa rubriker.
// Det kan finnas flera undergrupperingsnivåer, beroende på hur många gånger
// Text-egenskaperna för XE-fält segmenteras så här.
// Som standard kommer en INDEX-fältpostgrupp att skapa en ny rad för varje underrubrik inom denna grupp.
// Vi kan sätta flaggan RunSubentriesOnSameLine till true för att behålla rubriken,
// och varje underrubrik för gruppen på en rad istället, vilket gör INDEX-fältet mer kompakt.
index->set_RunSubentriesOnSameLine(runSubentriesOnTheSameLine);

if (runSubentriesOnTheSameLine)
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A \\r", index->GetFieldCode());
}
else
{
    ASSERT_EQ(u" INDEX  \\e \", see page \" \\h A", index->GetFieldCode());
}

// Infoga två XE-fält, vardera på en ny sida, och med samma rubrik benämnd "Heading 1",
// som INDEX-fältet kommer att använda för att gruppera dem.
// Om RunSubentriesOnSameLine är false, kommer INDEX‑tabellen att skapa tre rader:
// en rad för grupprubriken "Heading 1", och ytterligare en rad för varje underrubrik.
// Om RunSubentriesOnSameLine är true, kommer INDEX‑tabellen att skapa en enradig
// post som omfattar rubriken och varje underrubrik.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 1");

ASSERT_EQ(u" XE  \"Heading 1:Subheading 1\"", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Heading 1:Subheading 2");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + System::String::Format(u"Field.INDEX.XE.Subheading.docx"));
```

## Se även

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
