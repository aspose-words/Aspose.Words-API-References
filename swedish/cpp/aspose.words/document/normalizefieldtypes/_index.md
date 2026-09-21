---
title: "Aspose::Words::Document::NormalizeFieldTypes method"
linktitle: "NormalizeFieldTypes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::NormalizeFieldTypes method. Ändrar fälttypvärden FieldType för FieldStart, FieldSeparator, FieldEnd i hela dokumentet så att de motsvarar de fälttyper som finns i fältkoderna i C++."
type: docs
weight: 66000
url: /sv/cpp/aspose.words/document/normalizefieldtypes/
---
## Document::NormalizeFieldTypes method


Ändrar fälttypvärden [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) för [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) i hela dokumentet så att de motsvarar de fälttyper som finns i fältkoderna.

```cpp
void Aspose::Words::Document::NormalizeFieldTypes()
```

## Anmärkningar


Använd den här metoden efter dokumentändringar som påverkar fälttyper.

För att ändra fälttypvärden i en specifik del av dokumentet, använd [NormalizeFieldTypes](../../range/normalizefieldtypes/).

## Exempel



Visar hur man håller ett fälts typ uppdaterad med dess fältkod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words upptäcker automatiskt fälttyper baserat på fältkoder.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// Ändra manuellt fältets råa text, vilket bestämmer fältkoden.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// Att ändra fältkoden har ändrat detta fält till en annan typ,
// men fältets typ‑egenskaper visar fortfarande den gamla typen.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// Uppdatera dessa egenskaper med den här metoden för att visa det aktuella värdet.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## Se även

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
