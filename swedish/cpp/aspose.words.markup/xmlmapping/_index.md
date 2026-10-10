---
title: "Aspose::Words::Markup::XmlMapping klass"
linktitle: "XmlMapping"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::XmlMapping klass. Anger den information som används för att etablera en mappning mellan det överordnade strukturerade dokumenttagget och ett XML-element som lagras i en anpassad XML-datadelfil i dokumentet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 15000
url: /sv/cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


Specificerar den information som används för att etablera en mappning mellan den överordnade strukturerade dokumenttaggen och ett XML‑element som lagras i en anpassad XML‑datadel i dokumentet. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class XmlMapping : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Delete](./delete/)() | Tar bort mappning av det överordnade strukturerade dokumentet till XML-data. |
| [get_CustomXmlPart](./get_customxmlpart/)() | Returnerar den anpassade XML-datadelen som det överordnade strukturerade dokumenttagget är mappat till. |
| [get_IsMapped](./get_ismapped/)() | Returnerar **true** om det överordnade strukturerade dokumenttagget har mappats framgångsrikt till XML-data. |
| [get_PrefixMappings](./get_prefixmappings/)() const | Returnerar XML-namnrymdsprefix-mappningar för att utvärdera [XPath](./get_xpath/). |
| [get_StoreItemId](./get_storeitemid/)() | Anger identifieraren för den anpassade XML-datan för den anpassade XML-delfilen som ska användas för att utvärdera [XPath](./get_xpath/) uttrycket. |
| [get_XPath](./get_xpath/)() const | Returnerar XPath-uttrycket, som utvärderas för att hitta den anpassade XML-noden som är mappad till det överordnade strukturerade dokumenttagget. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | Ställer in en mappning mellan det överordnade strukturerade dokumenttagget och en XML-nod i en anpassad XML-datadelfil. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
