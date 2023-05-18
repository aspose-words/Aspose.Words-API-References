---
title: Aspose::Words::Fields::FieldIndex class
linktitle: FieldIndex
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldIndex class. Implements the INDEX field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 59000
url: /cpp/aspose.words.fields/fieldindex/
---
## FieldIndex class


Implements the INDEX field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldIndex : public Aspose::Words::Fields::Field,
                   public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Gets the name of the bookmark that marks the portion of the document used to build the index. |
| [get_CrossReferenceSeparator](./get_crossreferenceseparator/)() | Gets the character sequence that is used to separate cross references and other entries. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_EntryType](./get_entrytype/)() | Gets an index entry type used to build the index. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_HasPageNumberSeparator](./get_haspagenumberseparator/)() | Gets a value indicating whether a page number separator is overridden through the field's code. |
| [get_HasSequenceName](./get_hassequencename/)() | Gets a value indicating whether a sequence should be used while the field's result building. |
| [get_Heading](./get_heading/)() | Gets a heading that appears at the start of each set of entries for any given letter. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LanguageId](./get_languageid/)() | Gets the language ID used to generate the index. |
| [get_LetterRange](./get_letterrange/)() | Gets a range of letters to which limit the index. |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_NumberOfColumns](./get_numberofcolumns/)() | Gets the number of columns per page used when building the index. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Gets the character sequence that is used to separate two page numbers in a page number list. |
| [get_PageNumberSeparator](./get_pagenumberseparator/)() | Gets the character sequence that is used to separate an index entry and its page number. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Gets the character sequence that is used to separate the start and end of a page range. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/)() | Gets whether run subentries into the same line as the main entry. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SequenceName](./get_sequencename/)() | Gets the name of a sequence whose number is included with the page number. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_UseYomi](./get_useyomi/)() | Gets whether to enable the use of yomi text for index entries. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sets the name of the bookmark that marks the portion of the document used to build the index. |
| [set_CrossReferenceSeparator](./set_crossreferenceseparator/)(const System::String\&) | Sets the character sequence that is used to separate cross references and other entries. |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Sets an index entry type used to build the index. |
| [set_Heading](./set_heading/)(const System::String\&) | Sets a heading that appears at the start of each set of entries for any given letter. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Sets the language ID used to generate the index. |
| [set_LetterRange](./set_letterrange/)(const System::String\&) | Sets a range of letters to which limit the index. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberOfColumns](./set_numberofcolumns/)(const System::String\&) | Sets the number of columns per page used when building the index. |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Sets the character sequence that is used to separate two page numbers in a page number list. |
| [set_PageNumberSeparator](./set_pagenumberseparator/)(const System::String\&) | Sets the character sequence that is used to separate an index entry and its page number. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Sets the character sequence that is used to separate the start and end of a page range. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RunSubentriesOnSameLine](./set_runsubentriesonsameline/)(bool) | Sets whether run subentries into the same line as the main entry. |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Sets the name of a sequence whose number is included with the page number. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [set_UseYomi](./set_useyomi/)(bool) | Sets whether to enable the use of yomi text for index entries. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
