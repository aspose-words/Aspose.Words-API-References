---
title: "Aspose::Words::Document::NormalizeFieldTypes method"
linktitle: "NormalizeFieldTypes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::NormalizeFieldTypes method. Ändert Feldtypwerte FieldType von FieldStart, FieldSeparator, FieldEnd im gesamten Dokument, sodass sie den im Feldcode enthaltenen Feldtypen in C++ entsprechen."
type: docs
weight: 66000
url: /de/cpp/aspose.words/document/normalizefieldtypes/
---
## Document::NormalizeFieldTypes method


Ändert Feldtypwerte [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) von [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) im gesamten Dokument, sodass sie den im Feldcode enthaltenen Feldtypen entsprechen.

```cpp
void Aspose::Words::Document::NormalizeFieldTypes()
```

## Hinweise


Verwenden Sie diese Methode nach Dokumentänderungen, die Feldtypen beeinflussen.

Um Feldtypwerte in einem bestimmten Teil des Dokuments zu ändern, verwenden Sie [NormalizeFieldTypes](../../range/normalizefieldtypes/).

## Beispiele



Zeigt, wie man den Typ eines Feldes mit seinem Feldcode auf dem neuesten Stand hält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words erkennt Feldtypen automatisch anhand von Feldcodes.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// Ändern Sie den Rohtext des Feldes manuell, der den Feldcode bestimmt.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// Das Ändern des Feldcodes hat dieses Feld in einen anderen Typ umgewandelt,
// aber die Typ‑Eigenschaften des Feldes zeigen immer noch den alten Typ an.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// Aktualisieren Sie diese Eigenschaften mit dieser Methode, um den aktuellen Wert anzuzeigen.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
