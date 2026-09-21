---
title: "Aspose::Words::Fields::FieldOptions::get_TemplateName metod"
linktitle: "get_TemplateName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions::get_TemplateName metod. Hämtar eller anger filnamnet på den mall som används av dokumentet i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


Hämtar eller anger filnamnet på mallen som används av dokumentet.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## Anmärkningar


Denna egenskap används av [FieldTemplate](../../fieldtemplate/) fältet om [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) egenskapen är tom.

Om denna egenskap är tom används standardmallens filnamn **Normal.dotm**.

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

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
