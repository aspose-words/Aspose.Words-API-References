---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping-metod"
linktitle: "get_XmlMapping"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping-metod. Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttaggsintervall till XML-data i en anpassad XML-del av det aktuella dokumentet i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttaggsintervall till XML‑data i en anpassad XML‑del av det aktuella dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## Exempel



Visar hur man ställer in XML-mappningar för startintervallet av ett strukturerat dokumenttagg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// Skapa en XML-del som innehåller text och lägg till den i dokumentets CustomXmlPart-samling.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Skapa ett strukturerat dokumenttagg som kommer att visa innehållet i vår CustomXmlPart i dokumentet.
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// Om vi ställer in en mappning för vårt strukturerade dokumenttagg,
// kommer den endast att visa en del av CustomXmlPart som XPath pekar på.
// Detta XPath kommer att peka på innehållet i det andra "<text>"-elementet av det första "<root>"-elementet i vår CustomXmlPart.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## Se även

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
