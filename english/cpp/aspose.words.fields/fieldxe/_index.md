---
title: Aspose::Words::Fields::FieldXE class
linktitle: FieldXE
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldXE class. Implements the XE field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 111000
url: /cpp/aspose.words.fields/fieldxe/
---
## FieldXE class


Implements the XE field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldXE : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_EntryType](./get_entrytype/)() | Gets an index entry type. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsBold](./get_isbold/)() | Gets whether to apply bold formatting to the entry's page number. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsItalic](./get_isitalic/)() | Gets whether to apply italic formatting to the entry's page number. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_PageNumberReplacement](./get_pagenumberreplacement/)() | Gets text used in place of a page number. |
| [get_PageRangeBookmarkName](./get_pagerangebookmarkname/)() | Gets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_Text](./get_text/)() | Gets the text of the entry. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_Yomi](./get_yomi/)() | Gets the yomi (first phonetic character for sorting indexes) for the index entry. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Sets an index entry type. |
| [set_IsBold](./set_isbold/)(bool) | Sets whether to apply bold formatting to the entry's page number. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsItalic](./set_isitalic/)(bool) | Sets whether to apply italic formatting to the entry's page number. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberReplacement](./set_pagenumberreplacement/)(const System::String\&) | Sets text used in place of a page number. |
| [set_PageRangeBookmarkName](./set_pagerangebookmarkname/)(const System::String\&) | Sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_Text](./set_text/)(const System::String\&) | Sets the text of the entry. |
| [set_Yomi](./set_yomi/)(const System::String\&) | Sets the yomi (first phonetic character for sorting indexes) for the index entry. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
