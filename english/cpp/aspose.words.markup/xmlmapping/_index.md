---
title: Aspose::Words::Markup::XmlMapping class
linktitle: XmlMapping
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::XmlMapping class. Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document. To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class XmlMapping : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Delete](./delete/)() | Deletes mapping of the parent structured document to XML data. |
| [get_CustomXmlPart](./get_customxmlpart/)() | Returns the custom XML data part to which the parent structured document tag is mapped. |
| [get_IsMapped](./get_ismapped/)() | Returns **true** if the parent structured document tag is successfully mapped to XML data. |
| [get_PrefixMappings](./get_prefixmappings/)() const | Returns XML namespace prefix mappings to evaluate the [XPath](./get_xpath/). |
| [get_StoreItemId](./get_storeitemid/)() | Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [XPath](./get_xpath/) expression. |
| [get_XPath](./get_xpath/)() const | Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | Sets a mapping between the parent structured document tag and an XML node of a custom XML data part. |
| static [Type](./type/)() |  |

## Examples



Shows how to set XML mappings for custom XML parts. 
```cpp
auto doc = MakeObject<Document>();

// Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
String xmlPartId = System::Guid::NewGuid().ToString(u"B");
String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
SharedPtr<CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Create a structured document tag that will display the contents of our CustomXmlPart.
auto tag = MakeObject<StructuredDocumentTag>(doc, SdtType::PlainText, MarkupLevel::Block);

// Set a mapping for our structured document tag. This mapping will instruct
// our structured document tag to display a portion of the XML part's text contents that the XPath points to.
// In this case, it will be contents of the the second "<text>" element of the first "<root>" element: "Text element #2".
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// Add the structured document tag to the document to display the content from our custom part.
doc->get_FirstSection()->get_Body()->AppendChild(tag);
doc->Save(ArtifactsDir + u"StructuredDocumentTag.XmlMapping.docx");
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
