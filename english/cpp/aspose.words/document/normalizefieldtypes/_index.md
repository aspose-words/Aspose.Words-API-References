---
title: Aspose::Words::Document::NormalizeFieldTypes method
linktitle: NormalizeFieldTypes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::NormalizeFieldTypes method. Changes field type values FieldType of FieldStart, FieldSeparator, FieldEnd in the whole document so that they correspond to the field types contained in the field codes in C++.'
type: docs
weight: 66000
url: /cpp/aspose.words/document/normalizefieldtypes/
---
## Document::NormalizeFieldTypes method


Changes field type values [FieldType](../../../aspose.words.fields/fieldchar/get_fieldtype/) of [FieldStart](../../../aspose.words.fields/fieldstart/), [FieldSeparator](../../../aspose.words.fields/fieldseparator/), [FieldEnd](../../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes.

```cpp
void Aspose::Words::Document::NormalizeFieldTypes()
```

## Remarks


Use this method after document changes that affect field types.

To change field type values in a specific part of the document use [NormalizeFieldTypes](../../range/normalizefieldtypes/).

## Examples



Shows how to get the keep a field's type up to date with its field code. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE", nullptr);

// Aspose.Words automatically detects field types based on field codes.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());

// Manually change the raw text of the field, which determines the field code.
auto fieldText = System::ExplicitCast<Aspose::Words::Run>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(0));
fieldText->set_Text(u"PAGE");

// Changing the field code has changed this field to one of a different type,
// but the field's type properties still display the old type.
ASSERT_EQ(u"PAGE", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_End()->get_FieldType());

// Update those properties with this method to display current value.
doc->NormalizeFieldTypes();

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Type());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Start()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_Separator()->get_FieldType());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldPage, field->get_End()->get_FieldType());
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
