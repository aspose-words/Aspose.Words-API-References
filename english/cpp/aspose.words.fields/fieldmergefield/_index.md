---
title: FieldMergeField
second_title: Aspose.Words for C++ API Reference
description: Implements the MERGEFIELD field.
type: docs
weight: 859
url: /cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


Implements the MERGEFIELD field.

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldName](./get_fieldname/)() | Gets the name of a data field. |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | Returns just the name of the data field. Any prefix is stripped to the prefix property. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_IsMapped](./get_ismapped/)() | Gets whether this field is a mapped field. |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | Gets whether to enable character conversion for vertical formatting. |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_TextAfter](./get_textafter/)() | Gets the text to be inserted after the field if the field is not blank. |
| [get_TextBefore](./get_textbefore/)() | Gets the text to be inserted before the field if the field is not blank. |
| [get_Type](./get_type/)() const override | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_FieldName](./set_fieldname/)(const System::String\&) | Sets the name of a data field. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsMapped](./set_ismapped/)(bool) | Sets whether this field is a mapped field. |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | Sets whether to enable character conversion for vertical formatting. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TextAfter](./set_textafter/)(const System::String\&) | Sets the text to be inserted after the field if the field is not blank. |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | Sets the text to be inserted before the field if the field is not blank. |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
