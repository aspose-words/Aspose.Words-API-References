---
title: Aspose::Words::Fields::Field::GetFieldCode method
linktitle: GetFieldCode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::Field::GetFieldCode method. Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
```


## Examples



Shows how to insert a field into a document using a field code. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// This overload of the InsertField method automatically updates inserted fields.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


Shows how to get a field's field code. 
```cpp
// Open a document which contains a MERGEFIELD inside an IF field.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// There are two ways of getting a field's field code:
// 1 -  Omit its inner fields:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Include its inner fields:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// By default, the GetFieldCode method displays inner fields.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


Returns text between field start and field separator (or field end if there is no separator).

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** if child field codes should be included. |

## Examples



Shows how to get a field's field code. 
```cpp
// Open a document which contains a MERGEFIELD inside an IF field.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// There are two ways of getting a field's field code:
// 1 -  Omit its inner fields:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  Include its inner fields:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// By default, the GetFieldCode method displays inner fields.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## See Also

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
