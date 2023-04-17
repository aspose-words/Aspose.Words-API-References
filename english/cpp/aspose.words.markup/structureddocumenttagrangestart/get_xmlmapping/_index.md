---
title: Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping method
linktitle: get_XmlMapping
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping method. Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## Examples



Shows how to set XML mappings for the range start of a structured document tag. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Multi-section structured document tags.docx");

// Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
String xmlPartId = System::Guid::NewGuid().ToString(u"B");
String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
SharedPtr<CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Create a structured document tag that will display the contents of our CustomXmlPart in the document.
auto sdtRangeStart = System::DynamicCast<StructuredDocumentTagRangeStart>(doc->GetChild(NodeType::StructuredDocumentTagRangeStart, 0, true));

// If we set a mapping for our structured document tag,
// it will only display a portion of the CustomXmlPart that the XPath points to.
// This XPath will point to the contents second "<text>" element of the first "<root>" element of our CustomXmlPart.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(ArtifactsDir + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## See Also

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
