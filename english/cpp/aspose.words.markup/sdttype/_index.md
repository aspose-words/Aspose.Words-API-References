---
title: SdtType
second_title: Aspose.Words for C++ API Reference
description: Specifies the type of a structured document tag (SDT) node.
type: docs
weight: 261
url: /cpp/aspose.words.markup/sdttype/
---
## SdtType enum


Specifies the type of a structured document tag (SDT) node.

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | No type is assigned to the SDT. |
| Bibliography | 1 | The SDT represents a bibliography entry. |
| Citation | 2 | The SDT represents a citation. |
| Equation | 3 | The SDT represents an equation. |
| DropDownList | 4 | The SDT represents a drop down list when displayed in the document. |
| ComboBox | 5 | The SDT represents a combo box when displayed in the document. |
| Date | 6 | The SDT represents a date picker when displayed in the document. |
| BuildingBlockGallery | 7 | The SDT represents a building block gallery type. |
| DocPartObj | 8 | The SDT represents a document part type. |
| Group | 9 | The SDT represents a restricted grouping when displayed in the document. |
| Picture | 10 | The SDT represents a picture when displayed in the document. |
| RichText | 11 | The SDT represents a rich text box when displayed in the document. |
| PlainText | 12 | The SDT represents a plain text box when displayed in the document. |
| Checkbox | 13 | The SDT represents a checkbox when displayed in the document. |
| RepeatingSection | 14 | The SDT represents repeating section type when displayed in the document. |
| RepeatingSectionItem | 15 | The SDT represents repeating section item. |
| EntityPicker | 16 | The SDT represents an entity picker that allows the user to select an instance of an external content type. |


## Examples




Shows how to work with styles for content control elements. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
SharedPtr<Style> quoteStyle = doc->get_Styles()->idx_get(StyleIdentifier::Quote);
auto sdtPlainText = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Reference a style in the document by name:
auto sdtRichText = MakeObject<StructuredDocumentTag>(doc, SdtType::RichText, MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

SharedPtr<NodeCollection> tags = doc->GetChildNodes(NodeType::StructuredDocumentTag, true);

for (const auto& node : System::IterateOver(tags))
{
    auto sdt = System::DynamicCast<StructuredDocumentTag>(node);

    ASSERT_EQ(StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```


Shows how to fill a table with data from in an XML part. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(
    u"Books", String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" +
                  u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" +
                  u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// Create headers for data from the XML content.
SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// Create a table with a repeating section inside.
auto repeatingSectionSdt = MakeObject<StructuredDocumentTag>(doc, SdtType::RepeatingSection, MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", String::Empty);
table->AppendChild(repeatingSectionSdt);

// Add repeating section item inside the repeating section and mark it as a row.
// This table will have a row for each element that we can find in the XML document
// using the "/books[1]/book" XPath, of which there are three.
auto repeatingSectionItemSdt = MakeObject<StructuredDocumentTag>(doc, SdtType::RepeatingSectionItem, MarkupLevel::Row);
repeatingSectionSdt->AppendChild(repeatingSectionItemSdt);

auto row = MakeObject<Row>(doc);
repeatingSectionItemSdt->AppendChild(row);

// Map XML data with created table cells for the title and author of each book.
auto titleSdt = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", String::Empty);
row->AppendChild(titleSdt);

auto authorSdt = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", String::Empty);
row->AppendChild(authorSdt);

doc->Save(ArtifactsDir + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```

