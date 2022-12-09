---
title: BuiltInDocumentProperties
second_title: Aspose.Words for C++ API Reference
description: A collection of built-in document properties. To learn more, visit the  documentation article.
type: docs
weight: 1
url: /cpp/aspose.words.properties/builtindocumentproperties/
---
## BuiltInDocumentProperties class


A collection of built-in document properties. To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) documentation article.

```cpp
class BuiltInDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Methods

| Method | Description |
| --- | --- |
| [Clear](../documentpropertycollection/clear/)() | Removes all properties from the collection. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Returns **true** if a property with the specified name exists in the collection. |
| [get_Author](./get_author/)() | Gets or sets the name of the document's author. |
| [get_Bytes](./get_bytes/)() | Represents an estimate of the number of bytes in the document. |
| [get_Category](./get_category/)() | Gets or sets the category of the document. |
| [get_Characters](./get_characters/)() | Represents an estimate of the number of characters in the document. |
| [get_CharactersWithSpaces](./get_characterswithspaces/)() | Represents an estimate of the number of characters (including spaces) in the document. |
| [get_Comments](./get_comments/)() | Gets or sets the document comments. |
| [get_Company](./get_company/)() | Gets or sets the company property. |
| [get_ContentStatus](./get_contentstatus/)() | Gets or sets the [ContentStatus](../) of the document. |
| [get_ContentType](./get_contenttype/)() | Gets or sets the [ContentType](../) of the document. |
| [get_Count](../documentpropertycollection/get_count/)() | Gets number of items in the collection. |
| [get_CreatedTime](./get_createdtime/)() | Gets or sets date of the document creation in UTC. |
| [get_HeadingPairs](./get_headingpairs/)() | Specifies document headings and their names. |
| [get_HyperlinkBase](./get_hyperlinkbase/)() | Specifies the base string used for evaluating relative hyperlinks in this document. |
| [get_Keywords](./get_keywords/)() | Gets or sets the document keywords. |
| [get_LastPrinted](./get_lastprinted/)() | Gets or sets the date when the document was last printed in UTC. |
| [get_LastSavedBy](./get_lastsavedby/)() | Gets or sets the name of the last author. |
| [get_LastSavedTime](./get_lastsavedtime/)() | Gets or sets the time of the last save in UTC. |
| [get_Lines](./get_lines/)() | Represents an estimate of the number of lines in the document. |
| [get_LinksUpToDate](./get_linksuptodate/)() | Indicates whether hyperlinks in a document are up-to-date. |
| [get_Manager](./get_manager/)() | Gets or sets the manager property. |
| [get_NameOfApplication](./get_nameofapplication/)() | Gets or sets the name of the application. |
| [get_Pages](./get_pages/)() | Represents an estimate of the number of pages in the document. |
| [get_Paragraphs](./get_paragraphs/)() | Represents an estimate of the number of paragraphs in the document. |
| [get_RevisionNumber](./get_revisionnumber/)() | Gets or sets the document revision number. |
| [get_Security](./get_security/)() | Specifies the security level of a document as a numeric value. |
| [get_Subject](./get_subject/)() | Gets or sets the subject of the document. |
| [get_Template](./get_template/)() | Gets or sets the informational name of the document template. |
| [get_Thumbnail](./get_thumbnail/)() | Gets or sets the thumbnail of the document. |
| [get_Title](./get_title/)() | Gets or sets the title of the document. |
| [get_TitlesOfParts](./get_titlesofparts/)() | Each string in the array specifies the name of a part in the document. |
| [get_TotalEditingTime](./get_totaleditingtime/)() | Gets or sets the total editing time in minutes. |
| [get_Version](./get_version/)() | Represents the version number of the application that created the document. |
| [get_Words](./get_words/)() | Represents an estimate of the number of words in the document. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(System::String) override | Returns a [DocumentProperty](../documentproperty/) object by the name of the property. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | Returns a [DocumentProperty](../documentproperty/) object by index. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Gets the index of a property by name. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Removes a property with the specified name from the collection. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Removes a property at the specified index. |
| [set_Author](./set_author/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Author](./get_author/). |
| [set_Bytes](./set_bytes/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Bytes](./get_bytes/). |
| [set_Category](./set_category/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Category](./get_category/). |
| [set_Characters](./set_characters/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters](./get_characters/). |
| [set_CharactersWithSpaces](./set_characterswithspaces/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_CharactersWithSpaces](./get_characterswithspaces/). |
| [set_Comments](./set_comments/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments](./get_comments/). |
| [set_Company](./set_company/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Company](./get_company/). |
| [set_ContentStatus](./set_contentstatus/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_ContentStatus](./get_contentstatus/). |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_ContentType](./get_contenttype/). |
| [set_CreatedTime](./set_createdtime/)(System::DateTime) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime](./get_createdtime/). |
| [set_HeadingPairs](./set_headingpairs/)(const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs](./get_headingpairs/). |
| [set_HyperlinkBase](./set_hyperlinkbase/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase](./get_hyperlinkbase/). |
| [set_Keywords](./set_keywords/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords](./get_keywords/). |
| [set_LastPrinted](./set_lastprinted/)(System::DateTime) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted](./get_lastprinted/). |
| [set_LastSavedBy](./set_lastsavedby/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedBy](./get_lastsavedby/). |
| [set_LastSavedTime](./set_lastsavedtime/)(System::DateTime) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime](./get_lastsavedtime/). |
| [set_Lines](./set_lines/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines](./get_lines/). |
| [set_LinksUpToDate](./set_linksuptodate/)(bool) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_LinksUpToDate](./get_linksuptodate/). |
| [set_Manager](./set_manager/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Manager](./get_manager/). |
| [set_NameOfApplication](./set_nameofapplication/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication](./get_nameofapplication/). |
| [set_Pages](./set_pages/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Pages](./get_pages/). |
| [set_Paragraphs](./set_paragraphs/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Paragraphs](./get_paragraphs/). |
| [set_RevisionNumber](./set_revisionnumber/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber](./get_revisionnumber/). |
| [set_Security](./set_security/)(Aspose::Words::Properties::DocumentSecurity) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Security](./get_security/). |
| [set_Subject](./set_subject/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Subject](./get_subject/). |
| [set_Template](./set_template/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Template](./get_template/). |
| [set_Thumbnail](./set_thumbnail/)(const System::ArrayPtr\<uint8_t\>\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail](./get_thumbnail/). |
| [set_Title](./set_title/)(const System::String\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Title](./get_title/). |
| [set_TitlesOfParts](./set_titlesofparts/)(const System::ArrayPtr\<System::String\>\&) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts](./get_titlesofparts/). |
| [set_TotalEditingTime](./set_totaleditingtime/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_TotalEditingTime](./get_totaleditingtime/). |
| [set_Version](./set_version/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Version](./get_version/). |
| [set_Words](./set_words/)(int32_t) | Setter for [Aspose::Words::Properties::BuiltInDocumentProperties::get_Words](./get_words/). |
| static [Type](./type/)() |  |
## Remarks


Provides access to [DocumentProperty](../documentproperty/) objects by their names (using an indexer) and via a set of typed properties that return values of appropriate types.

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.

## Examples



Shows how to work with built-in document properties. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Properties.docx");

// The "Document" object contains some of its metadata in its members.
std::cout << "Document filename:\n\t \"" << doc->get_OriginalFileName() << "\"" << std::endl;

// The document also stores metadata in its built-in properties.
// Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
std::cout << "Built-in Properties:" << std::endl;
for (const auto& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Some properties may store multiple values.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (const auto& value : System::IterateOver(
                 System::DynamicCast_noexcept<System::Collections::Generic::ICollection<SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << "\tValue:\t\"" << value << "\"" << std::endl;
        }
    }
    else
    {
        std::cout << "\tValue:\t\"" << docProperty->get_Value() << "\"" << std::endl;
    }
}
```

## See Also

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words](../../)
