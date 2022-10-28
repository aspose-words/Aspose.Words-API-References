---
title: FieldUnknown
second_title: Aspose.Words for C++ API Reference
description: Implements an unknown or unrecognized field.
type: docs
weight: 1366
url: /cpp/aspose.words.fields/fieldunknown/
---
## FieldUnknown class


Implements an unknown or unrecognized field.

```cpp
class FieldUnknown : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](./get_end/)() override | Gets the node that represents the field end. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](./get_separator/)() override | Gets the node that represents the field separator. Can be null. |
| [get_Start](./get_start/)() override | Gets the node that represents the start of the field. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples




Shows how to work with 'FieldNone' field in a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a field that does not denote an objective field type in its field code.
SharedPtr<Field> field = builder->InsertField(u" NOTAREALFIELD //a");

// The "FieldNone" field type is reserved for fields such as these.
ASSERT_EQ(FieldType::FieldNone, field->get_Type());

// We can also still work with these fields and assign them as instances of the FieldUnknown class.
auto fieldUnknown = System::DynamicCast<FieldUnknown>(field);
ASSERT_EQ(u" NOTAREALFIELD //a", fieldUnknown->GetFieldCode());
```

