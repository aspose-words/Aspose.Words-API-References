---
title: "Aspose::Words::Fields::FieldOptions::get_FileName metod"
linktitle: "get_FileName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions::get_FileName metod. Hämtar eller anger filnamnet på dokumentet i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.fields/fieldoptions/get_filename/
---
## FieldOptions::get_FileName method


Hämtar eller anger filnamnet på dokumentet.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_FileName() const
```

## Anmärkningar


Den här egenskapen används av fältet [FieldFileName](../../fieldfilename/) med högre prioritet än egenskapen [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## Exempel



Visar hur man använder [FieldOptions](../) för att åsidosätta standardvärdet för FILENAME-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// Detta FILENAME-fält kommer att visa det lokala systemfilnamnet för dokumentet vi laddade.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// Som standard visar FILENAME-fältet filens namn, men inte dess fullständiga lokala filsökväg.
// Vi kan sätta en flagga för att få den att visa hela filsökvägen.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// Vi kan också sätta ett värde för denna egenskap till
// åsidosätta värdet som FILENAME-fältet visar.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## Se även

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
