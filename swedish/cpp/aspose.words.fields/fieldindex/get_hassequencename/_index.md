---
title: "Aspose::Words::Fields::FieldIndex::get_HasSequenceName metod"
linktitle: "get_HasSequenceName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIndex::get_HasSequenceName metod. Hämtar ett värde som indikerar om en sekvens ska användas medan fältets resultat byggs i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.fields/fieldindex/get_hassequencename/
---
## FieldIndex::get_HasSequenceName method


Hämtar ett värde som indikerar om en sekvens ska användas under fältets resultatbyggnad.

```cpp
bool Aspose::Words::Fields::FieldIndex::get_HasSequenceName()
```


## Exempel



Visar hur man delar ett dokument i delar genom att kombinera INDEX‑ och SEQ‑fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
// och sidnumret som innehåller XE-fältet på höger sida.
// Om XE-fälten har samma värde i deras \"Text\"-egenskap,
// kommer INDEX-fältet att gruppera dem till en post.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// I egenskapen SequenceName anger du en SEQ‑fältsekvens. Varje post i detta INDEX‑fält kommer nu också att visa
// numret som sekvensräkningen har på XE‑fältets plats som skapade denna post.
index->set_SequenceName(u"MySequence");

// Ange text som omger sekvens‑ och sidnumren för att förklara deras betydelse för användaren.
// En post som skapats med denna konfiguration kommer att visa något i stil med "MySequence at 1 on page 1" vid dess sidnummer.
// PageNumberSeparator och SequenceSeparator får inte vara längre än 15 tecken.
index->set_PageNumberSeparator(u"\tMySequence at ");
index->set_SequenceSeparator(u" on page ");
ASSERT_TRUE(index->get_HasSequenceName());

ASSERT_EQ(u" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index->GetFieldCode());

// SEQ-fält visar ett antal som ökas vid varje SEQ-fält.
// Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
// identifierade av SEQ-fältets "SequenceIdentifier"-egenskap.
// Infoga ett SEQ‑fält som flyttar "MySequence"‑sekvensen till 1.
// Detta fält är inte annorlunda än vanlig dokumenttext. Det kommer inte att visas i ett INDEX‑fältets innehållsförteckning.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", sequenceField->GetFieldCode());

// Infoga ett XE‑fält som skapar en post i INDEX‑fältet.
// Eftersom "MySequence" är på 1 och detta XE‑fält är på sida 2, tillsammans med de anpassade avgränsarna vi definierade ovan,
// kommer detta fälts INDEX‑post att visa "Cat" på vänster sida och "MySequence at 1 on page 2" på höger sida.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

ASSERT_EQ(u" XE  Cat", indexEntry->GetFieldCode());

// Infoga en sidbrytning och använd SEQ‑fält för att avancera "MySequence" till 3.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");
sequenceField = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
sequenceField->set_SequenceIdentifier(u"MySequence");

// Infoga ett XE‑fält med samma Text‑egenskap som ovan.
// INDEX‑posten kommer att gruppera XE‑fält med matchande värden i "Text"‑egenskapen
// till en post istället för att skapa en post för varje XE-fält.
// Eftersom vi är på sida 2 med "MySequence" på 3, kommer ", 3 on page 3" att läggas till i samma INDEX‑post som ovan.
// Sidnumrets del av den INDEX‑posten kommer nu att visa "MySequence at 1 on page 2, 3 on page 3".
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cat");

// Infoga ett XE‑fält med ett nytt och unikt Text‑egenskapsvärde.
// Detta kommer att lägga till en ny post, med MySequence på 3 på sida 4.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Dog");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Sequence.docx");
```

## Se även

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
