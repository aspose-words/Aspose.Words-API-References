---
title: Aspose::Words::Fields::FieldCitation class
linktitle: FieldCitation
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldCitation class. Implements the CITATION field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


Implements the CITATION field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Gets a value that matches the **Tag** element's value of another source to be included in the citation. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Gets the language ID that is used in conjunction with the specified bibliographic style to format the citation in the document. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_PageNumber](./get_pagenumber/)() | Gets a page number associated with the citation. |
| [get_Prefix](./get_prefix/)() | Gets a prefix that is prepended to the citation. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SourceTag](./get_sourcetag/)() | Gets a value that matches the **Tag** element's value of the source to insert. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_Suffix](./get_suffix/)() | Gets a suffix that is appended to the citation. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Gets whether the author information is suppressed from the citation. |
| [get_SuppressTitle](./get_suppresstitle/)() | Gets whether the title information is suppressed from the citation. |
| [get_SuppressYear](./get_suppressyear/)() | Gets whether the year information is suppressed from the citation. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_VolumeNumber](./get_volumenumber/)() | Gets a volume number associated with the citation. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Sets a value that matches the **Tag** element's value of another source to be included in the citation. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Sets the language ID that is used in conjunction with the specified bibliographic style to format the citation in the document. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Sets a page number associated with the citation. |
| [set_Prefix](./set_prefix/)(const System::String\&) | Sets a prefix that is prepended to the citation. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Sets a value that matches the **Tag** element's value of the source to insert. |
| [set_Suffix](./set_suffix/)(const System::String\&) | Sets a suffix that is appended to the citation. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Sets whether the author information is suppressed from the citation. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Sets whether the title information is suppressed from the citation. |
| [set_SuppressYear](./set_suppressyear/)(bool) | Sets whether the year information is suppressed from the citation. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Sets a volume number associated with the citation. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
