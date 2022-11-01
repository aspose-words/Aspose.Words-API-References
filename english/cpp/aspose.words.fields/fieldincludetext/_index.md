---
title: FieldIncludeText
second_title: Aspose.Words for C++ API Reference
description: Implements the INCLUDETEXT field.
type: docs
weight: 742
url: /cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


Implements the INCLUDETEXT field.

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field, public Aspose::Words::Fields::IFieldCodeTokenInfoProvider, public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Methods

| Method | Description |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Gets or sets the name of the bookmark in the document to include. |
| [get_DisplayResult](../field/get_displayresult/)() | Gets the text that represents the displayed field result. |
| [get_Encoding](./get_encoding/)() | Gets or sets the encoding applied to the data within the referenced file. |
| [get_End](../field/get_end/)() const | Gets the node that represents the field end. |
| [get_FieldEnd](../field/get_fieldend/)() const | Gets the node that represents the field end. |
| [get_FieldStart](../field/get_fieldstart/)() const | Gets the node that represents the start of the field. |
| [get_Format](../field/get_format/)() | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting. |
| [get_IsDirty](../field/get_isdirty/)() | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../field/get_islocked/)() | Gets or sets whether the field is locked (should not recalculate its result). |
| [get_LocaleId](../field/get_localeid/)() | Gets or sets the LCID of the field. |
| [get_LockFields](./get_lockfields/)() override | Gets or sets whether to prevent fields in the included document from being updated. |
| [get_MimeType](./get_mimetype/)() | Gets or sets the MIME type of the referenced file. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | Gets or sets the namespace mappings for XPath queries. |
| [get_Result](../field/get_result/)() | Gets or sets text that is between the field separator and field end. |
| [get_Separator](../field/get_separator/)() | Gets the node that represents the field separator. Can be null. |
| [get_SourceFullName](./get_sourcefullname/)() override | Gets or sets the location of the document using an IRI. |
| [get_Start](../field/get_start/)() const | Gets the node that represents the start of the field. |
| [get_TextConverter](./get_textconverter/)() override | Gets or sets the name of the text converter for the format of the included file. |
| virtual [get_Type](../field/get_type/)() const | Gets the Microsoft Word field type. |
| [get_XPath](./get_xpath/)() override | Gets or sets XPath for the desired portion of the XML file. |
| [get_XslTransformation](./get_xsltransformation/)() override | Gets or sets the location of XSL Transformation to format XML data. |
| [GetFieldCode](../field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_BookmarkName](./get_bookmarkname/). |
| [set_Encoding](./set_encoding/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_Encoding](./get_encoding/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter for [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter for [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_LockFields](./get_lockfields/). |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_MimeType](./get_mimetype/). |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_NamespaceMappings](./get_namespacemappings/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter for [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_SourceFullName](./get_sourcefullname/). |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_TextConverter](./get_textconverter/). |
| [set_XPath](./set_xpath/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_XPath](./get_xpath/). |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | Setter for [Aspose::Words::Fields::FieldIncludeText::get_XslTransformation](./get_xsltransformation/). |
| [Unlink](../field/unlink/)() | Performs the field unlink. |
| [Update](../field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../field/update/)(bool) | Performs a field update. Throws if the field is being updated already. |

## Examples




Shows how to create an INCLUDETEXT field, and set its properties. 
```cpp
void FieldIncludeText_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
    // 1 -  Perform an XSL transformation on an XML document:
    SharedPtr<FieldIncludeText> fieldIncludeText =
        CreateFieldIncludeText(builder, MyDir + u"CD collection data.xml", false, u"text/xml", u"XML", u"ISO-8859-1");
    fieldIncludeText->set_XslTransformation(MyDir + u"CD collection XSL transformation.xsl");

    builder->Writeln();

    // 2 -  Use an XPath to take specific elements from an XML document:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + u"CD collection data.xml", false, u"text/xml", u"XML", u"ISO-8859-1");
    fieldIncludeText->set_NamespaceMappings(u"xmlns:n='myNamespace'");
    fieldIncludeText->set_XPath(u"/catalog/cd/title");

    doc->Save(ArtifactsDir + u"Field.INCLUDETEXT.docx");
}

SharedPtr<FieldIncludeText> CreateFieldIncludeText(SharedPtr<DocumentBuilder> builder, String sourceFullName, bool lockFields, String mimeType,
                                                   String textConverter, String encoding)
{
    auto fieldIncludeText = System::DynamicCast<FieldIncludeText>(builder->InsertField(FieldType::FieldIncludeText, true));
    fieldIncludeText->set_SourceFullName(sourceFullName);
    fieldIncludeText->set_LockFields(lockFields);
    fieldIncludeText->set_MimeType(mimeType);
    fieldIncludeText->set_TextConverter(textConverter);
    fieldIncludeText->set_Encoding(encoding);

    return fieldIncludeText;
}
```

