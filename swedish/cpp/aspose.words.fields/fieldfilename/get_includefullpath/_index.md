---
title: "Aspose::Words::Fields::FieldFileName::get_IncludeFullPath-metoden"
linktitle: "get_IncludeFullPath"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldFileName::get_IncludeFullPath-metoden. Hämtar eller anger om hela filsökvägsnamnet ska inkluderas i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldfilename/get_includefullpath/
---
## FieldFileName::get_IncludeFullPath method


Hämtar eller anger om hela filsökvägsnamnet ska inkluderas.

```cpp
bool Aspose::Words::Fields::FieldFileName::get_IncludeFullPath()
```


## Exempel



Visar hur man använder [FieldOptions](../../fieldoptions/) för att åsidosätta standardvärdet för FILENAME-fältet.
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

* Class [FieldFileName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
