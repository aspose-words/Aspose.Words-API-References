---
title: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath metod"
linktitle: "get_IncludeFullPath"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath metod. Hämtar eller anger om hela filsökvägsnamnet ska inkluderas i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


Hämtar eller anger om hela filsökvägsnamnet ska inkluderas.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


## Exempel



Visar hur man använder ett TEMPLATE-fält för att visa den lokala filsystemplatsen för ett dokuments mall.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Vi kan ange ett mallnamn som används av fälten. Denna egenskap används när "doc.AttachedTemplate" är tom.
// Om denna egenskap är tom används standardmallens filnamn "Normal.dotm".
doc->get_FieldOptions()->set_TemplateName(System::String::Empty);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TEMPLATE.docx");
```

## Se även

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
