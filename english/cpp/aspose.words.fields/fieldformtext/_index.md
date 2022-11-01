---
title: FieldFormText
second_title: Aspose.Words for C++ API Reference
description: Implements the FORMTEXT field.
type: docs
weight: 612
url: /cpp/aspose.words.fields/fieldformtext/
---
## FieldFormText class


Implements the FORMTEXT field.

```cpp
class FieldFormText : public Aspose::Words::Fields::Field
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
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




Shows how to process FORMCHECKBOX, FORMDROPDOWN and FORMTEXT fields. 
```cpp
// These fields are legacy equivalents of the FormField. We can read, but not create these fields using Aspose.Words.
// In Microsoft Word, we can insert these fields via the Legacy Tools menu in the Developer tab.
auto doc = MakeObject<Document>(MyDir + u"Form fields.docx");

auto fieldFormCheckBox = System::DynamicCast<FieldFormCheckBox>(doc->get_Range()->get_Fields()->idx_get(1));
ASSERT_EQ(u" FORMCHECKBOX \u0001", fieldFormCheckBox->GetFieldCode());

auto fieldFormDropDown = System::DynamicCast<FieldFormDropDown>(doc->get_Range()->get_Fields()->idx_get(2));
ASSERT_EQ(u" FORMDROPDOWN \u0001", fieldFormDropDown->GetFieldCode());

auto fieldFormText = System::DynamicCast<FieldFormText>(doc->get_Range()->get_Fields()->idx_get(0));
ASSERT_EQ(u" FORMTEXT \u0001", fieldFormText->GetFieldCode());
```

