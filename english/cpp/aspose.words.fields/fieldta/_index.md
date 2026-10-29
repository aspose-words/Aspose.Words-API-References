---
title: Aspose::Words::Fields::FieldTA class
linktitle: FieldTA
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldTA class. Implements the TA field. To learn more, visit the Working with Fields documentation article in C++.'
type: docs
weight: 99000
url: /cpp/aspose.words.fields/fieldta/
---
## FieldTA class


Implements the TA field. 
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldTA : public Field,
                public IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_EntryCategory](./get_entrycategory/)() | Gets or sets the integral entry category, which is a number that corresponds to the order of categories. |
| [get_IsBold](./get_isbold/)() | Gets whether to apply bold formatting to the page number for the entry. |
| [get_IsItalic](./get_isitalic/)() | Gets whether to apply italic formatting to the page number for the entry. |
| [get_LongCitation](./get_longcitation/)() | Gets the long citation for the entry. |
| [get_PageRangeBookmarkName](./get_pagerangebookmarkname/)() | Gets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [get_ShortCitation](./get_shortcitation/)() | Gets the short citation for the entry. |
| [set_EntryCategory](./set_entrycategory/)(const System::String \&) | Sets the integral entry category, which is a number that corresponds to the order of categories. |
| [set_IsBold](./set_isbold/)(bool) | Sets whether to apply bold formatting to the page number for the entry. |
| [set_IsItalic](./set_isitalic/)(bool) | Sets whether to apply italic formatting to the page number for the entry. |
| [set_LongCitation](./set_longcitation/)(const System::String \&) | Sets the long citation for the entry. |
| [set_PageRangeBookmarkName](./set_pagerangebookmarkname/)(const System::String \&) | Sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [set_ShortCitation](./set_shortcitation/)(const System::String \&) | Sets the short citation for the entry. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| virtual [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Sets whether the field is locked (should not recalculate its result). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sets the LCID of the field. |
| [set_Result](../field/set_result/)(const System::String \&) | Sets text that is between the field separator and field end. |
## Remarks

 Defines the text and page number for a table of authorities entry, which is used by a TOA field. 
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
