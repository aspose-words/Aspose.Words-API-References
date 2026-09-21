---
title: "Aspose::Words::Markup::XmlMapping::get_IsMapped‑metod"
linktitle: "get_IsMapped"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::XmlMapping::get_IsMapped‑metod. Returnerar true om den överordnade structured document tag har mappats framgångsrikt till XML‑data i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.markup/xmlmapping/get_ismapped/
---
## XmlMapping::get_IsMapped method


Returnerar **true** om det överordnade strukturerade dokumenttagget har mappats framgångsrikt till XML-data.

```cpp
bool Aspose::Words::Markup::XmlMapping::get_IsMapped()
```


## Exempel



Visar hur man ställer in XML-mappningar för anpassade XML-delar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa en XML-del som innehåller text och lägg till den i dokumentets CustomXmlPart-samling.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Skapa ett strukturerat dokumenttagg som kommer att visa innehållet i vår CustomXmlPart.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// Ställ in en mappning för vår strukturerade dokumenttagg. Denna mappning kommer att instruera
// vår strukturerade dokumenttagg att visa en del av XML-delens textinnehåll som XPath pekar på.
// I det här fallet kommer det att vara innehållet i det andra "<text>"-elementet i det första "<root>"-elementet: "Text element #2".
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// Lägg till den strukturerade dokumenttaggen i dokumentet för att visa innehållet från vår anpassade del.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## Se även

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
