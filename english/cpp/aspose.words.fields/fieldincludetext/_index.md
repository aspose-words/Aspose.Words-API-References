---
title: Aspose::Words::Fields::FieldIncludeText class
linktitle: FieldIncludeText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldIncludeText class. Implements the INCLUDETEXT field. To learn more, visit the  documentation article in C++.'
type: docs
weight: 58000
url: /cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


Implements the INCLUDETEXT field. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Gets the name of the bookmark in the document to include. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_Encoding](./get_encoding/)() | Gets the encoding applied to the data within the referenced file. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_LockFields](./get_lockfields/)() override | Gets whether to prevent fields in the included document from being updated. |
| [get_MimeType](./get_mimetype/)() | Gets the MIME type of the referenced file. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | Gets the namespace mappings for XPath queries. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Gets the location of the document using an IRI. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_TextConverter](./get_textconverter/)() override | Gets the name of the text converter for the format of the included file. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_XPath](./get_xpath/)() override | Gets XPath for the desired portion of the XML file. |
| [get_XslTransformation](./get_xsltransformation/)() override | Gets the location of XSL Transformation to format XML data. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sets the name of the bookmark in the document to include. |
| [set_Encoding](./set_encoding/)(const System::String\&) | Sets the encoding applied to the data within the referenced file. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Sets whether to prevent fields in the included document from being updated. |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Sets the MIME type of the referenced file. |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | Sets the namespace mappings for XPath queries. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Sets the location of the document using an IRI. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Sets the name of the text converter for the format of the included file. |
| [set_XPath](./set_xpath/)(const System::String\&) | Sets XPath for the desired portion of the XML file. |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | Sets the location of XSL Transformation to format XML data. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |
## See Also

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
