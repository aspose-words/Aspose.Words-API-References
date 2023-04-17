---
title: Aspose::Words::Fields::FieldDatabase class
linktitle: FieldDatabase
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldDatabase class. Implements the DATABASE field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 28000
url: /cpp/aspose.words.fields/fielddatabase/
---
## FieldDatabase class


Implements the DATABASE field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldDatabase : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [FieldDatabase](./fielddatabase/)() |  |
| [get_Connection](./get_connection/)() | Gets a connection to the data. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_FileName](./get_filename/)() | Gets the complete path and file name of the database. |
| [get_FirstRecord](./get_firstrecord/)() | Gets the integral record number of the first data record to insert. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_FormatAttributes](./get_formatattributes/)() | Gets which attributes of the format are to be applied to the table. |
| [get_InsertHeadings](./get_insertheadings/)() | Gets whether to insert the field names from the database as column headings in the resulting table. |
| [get_InsertOnceOnMailMerge](./get_insertonceonmailmerge/)() | Gets whether to insert data at the beginning of a merge. |
| [get_IsDirty](../field/get_isdirty/)() | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LastRecord](./get_lastrecord/)() | Gets the integral record number of the last data record to insert. |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_Query](./get_query/)() | Gets a set of SQL instructions that query the database. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_TableFormat](./get_tableformat/)() | Gets the format that is to be applied to the result of the database query. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_Connection](./set_connection/)(const System::String\&) | Sets a connection to the data. |
| [set_FileName](./set_filename/)(const System::String\&) | Sets the complete path and file name of the database. |
| [set_FirstRecord](./set_firstrecord/)(const System::String\&) | Sets the integral record number of the first data record to insert. |
| [set_FormatAttributes](./set_formatattributes/)(const System::String\&) | Sets which attributes of the format are to be applied to the table. |
| [set_InsertHeadings](./set_insertheadings/)(bool) | Sets whether to insert the field names from the database as column headings in the resulting table. |
| [set_InsertOnceOnMailMerge](./set_insertonceonmailmerge/)(bool) | Sets whether to insert data at the beginning of a merge. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LastRecord](./set_lastrecord/)(const System::String\&) | Sets the integral record number of the last data record to insert. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Query](./set_query/)(const System::String\&) | Sets a set of SQL instructions that query the database. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TableFormat](./set_tableformat/)(const System::String\&) | Sets the format that is to be applied to the result of the database query. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
