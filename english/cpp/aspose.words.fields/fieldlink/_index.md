---
title: Aspose::Words::Fields::FieldLink class
linktitle: FieldLink
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldLink class. Implements the LINK field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 63000
url: /cpp/aspose.words.fields/fieldlink/
---
## FieldLink class


Implements the LINK field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldLink : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methods

| Method | Description |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Gets whether to update this field automatically. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_FormatUpdateType](./get_formatupdatetype/)() | Gets a way the linked object updates its formatting. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Gets whether to insert the linked object as a bitmap. |
| [get_InsertAsHtml](./get_insertashtml/)() | Gets whether to insert the linked object as HTML format text. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Gets whether to insert the linked object as a picture. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Gets whether to insert the linked object in rich-text format (RTF). |
| [get_InsertAsText](./get_insertastext/)() | Gets whether to insert the linked object in text-only format. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Gets whether to insert the linked object as Unicode text. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLinked](./get_islinked/)() | Gets whether to reduce the file size by not storing graphics data with the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_ProgId](./get_progid/)() | Gets the application type of the link information. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SourceFullName](./get_sourcefullname/)() | Gets the name and location of the source file. |
| [get_SourceItem](./get_sourceitem/)() | Gets the portion of the source file that's being linked. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Sets whether to update this field automatically. |
| [set_FormatUpdateType](./set_formatupdatetype/)(const System::String\&) | Sets a way the linked object updates its formatting. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Sets whether to insert the linked object as a bitmap. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Sets whether to insert the linked object as HTML format text. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Sets whether to insert the linked object as a picture. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Sets whether to insert the linked object in rich-text format (RTF). |
| [set_InsertAsText](./set_insertastext/)(bool) | Sets whether to insert the linked object in text-only format. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Sets whether to insert the linked object as Unicode text. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Sets whether to reduce the file size by not storing graphics data with the document. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Sets the application type of the link information. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Sets the name and location of the source file. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Sets the portion of the source file that's being linked. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
