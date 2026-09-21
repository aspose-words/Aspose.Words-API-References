---
title: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator metod"
linktitle: "get_CrossReferenceSeparator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator metod. Hämtar eller anger teckensekvensen som används för att separera korsreferenser och andra poster i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldindex/get_crossreferenceseparator/
---
## FieldIndex::get_CrossReferenceSeparator method


Hämtar eller anger teckensekvensen som används för att separera korsreferenser och andra poster.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator()
```


## Exempel



Visar hur man definierar korsreferenser i ett INDEX-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
// och sidnumret som innehåller XE-fältet på höger sida.
// INDEX-posten kommer att samla alla XE-fält med matchande värden i egenskapen "Text".
// till en post istället för att skapa en post för varje XE-fält.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Vi kan konfigurera ett XE-fält så att dess INDEX-post visar en sträng i stället för ett sidnummer.
// Först, för poster som ersätter ett sidnummer med en sträng,
// ange en anpassad avgränsare mellan XE-fältets Text‑egenskapsvärde och strängen.
index->set_CrossReferenceSeparator(u", see: ");

ASSERT_EQ(u" INDEX  \\k \", see: \"", index->GetFieldCode());

// Infoga ett XE-fält som skapar en vanlig INDEX-post som visar detta fälts sidnummer,
// och anropar inte värdet CrossReferenceSeparator.
// Posten för detta XE-fält kommer att visa "Apple, 2".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");

ASSERT_EQ(u" XE  Apple", indexEntry->GetFieldCode());

// Infoga ett annat XE-fält på sida 3 och ange ett värde för egenskapen PageNumberReplacement.
// Detta värde kommer att visas i stället för numret på den sida som detta fält är på,
// och INDEX-fältets CrossReferenceSeparator‑värde kommer att visas framför det.
// Posten för detta XE-fält kommer att visa "Banana, see: Tropical fruit".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");
indexEntry->set_PageNumberReplacement(u"Tropical fruit");

ASSERT_EQ(u" XE  Banana \\t \"Tropical fruit\"", indexEntry->GetFieldCode());

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.CrossReferenceSeparator.docx");
```

## Se även

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
