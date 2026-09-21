---
title: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter metod"
linktitle: "get_SeparatorCharacter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter metod. Hämtar eller anger separator‑tecknet som ska användas i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


Hämtar eller anger tecknet som ska användas som avgränsare.

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## Exempel



Visar hur man numrerar stycken med autonum-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Varje AUTONUM-fält visar det aktuella värdet av en löpande räkning av AUTONUM-fält,
// vilket gör att vi automatiskt kan numrera objekt som en numrerad lista.
// Detta fält kommer att visa siffran "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// Avgränsartecknet, som visas i fältresultatet omedelbart efter siffran, är som standard en punkt.
// Om vi lämnar denna egenskap null, kommer vårt andra AUTONUM-fält att visa "2." i dokumentet.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// Vi kan sätta denna egenskap så att det första tecknet i dess sträng används som det nya avgränsartecknet.
// I det här fallet kommer vårt AUTONUM-fält nu att visa "2:".
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## Se även

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
