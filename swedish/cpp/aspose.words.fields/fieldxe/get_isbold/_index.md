---
title: "Aspose::Words::Fields::FieldXE::get_IsBold metod"
linktitle: "get_IsBold"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldXE::get_IsBold metod. Hämtar eller anger om fet formatering ska tillämpas på postens sidnummer i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldxe/get_isbold/
---
## FieldXE::get_IsBold method


Hämtar eller anger om fet formatering ska tillämpas på postens sidnummer.

```cpp
bool Aspose::Words::Fields::FieldXE::get_IsBold()
```


## Exempel



Visar hur man fyller ett INDEX-fält med poster med hjälp av XE-fält, och även ändrar dess utseende.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
// och sidnumret som innehåller XE-fältet på höger sida.
// Om XE-fälten har samma värde i deras \"Text\"-egenskap,
// kommer INDEX-fältet att gruppera dem till en post.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Om du sätter detta egenskapsvärde till "A" kommer alla poster att grupperas efter deras första bokstav,
// och placera den bokstaven i versaler ovanför varje grupp.
index->set_Heading(u"A");

// Ställ in tabellen som skapats av INDEX-fältet så att den sträcker sig över 2 kolumner.
index->set_NumberOfColumns(u"2");

// Ställ in att alla poster med startbokstäver utanför teckenområdet "a-c" ska utelämnas.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// Dessa två nästa XE-fält kommer att visas under rubriken "A",
// med deras respektive textstilar också tillämpade på deras sidnummer.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Båda de två nästa XE-fälten kommer att vara under rubrikerna "B" och "C" i INDEX-fälten innehållsförteckning.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// INDEX-fält sorterar alla poster alfabetiskt, så denna post kommer att visas under "A" tillsammans med de andra två.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Denna post kommer inte att visas eftersom den börjar med bokstaven "D",
// vilket ligger utanför teckenområdet "a-c" som INDEX-fältets LetterRange-egenskap definierar.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Se även

* Class [FieldXE](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
