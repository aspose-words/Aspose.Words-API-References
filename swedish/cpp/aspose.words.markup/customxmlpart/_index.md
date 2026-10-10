---
title: "Aspose::Words::Markup::CustomXmlPart klass"
linktitle: "CustomXmlPart"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomXmlPart klass. Representerar en Custom XML Data Storage Part (anpassad XML-data inom ett paket). För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class


Representerar en anpassad XML‑datalagringsdel (anpassad XML‑data inom ett paket). För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPart : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clone](./clone/)() | Skapar en "tillräckligt djup" kopia av objektet. Duplicerar inte byte av [Data](./get_data/) värdet. |
| [CustomXmlPart](./customxmlpart/)() |  |
| [get_Data](./get_data/)() const | Hämtar eller anger XML-innehållet för denna Custom XML Data Storage Part. |
| [get_DataChecksum](./get_datachecksum/)() | Anger en cyclic redundancy check (CRC) kontrollsumma för [Data](./get_data/) innehållet. |
| [get_Id](./get_id/)() const | Hämtar eller anger strängen som identifierar denna anpassade XML-del inom ett OOXML-dokument. |
| [get_Schemas](./get_schemas/)() const | Anger uppsättningen av XML-scheman som är associerade med denna anpassade XML-del. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Sättare för [Aspose::Words::Markup::CustomXmlPart::get_Data](./get_data/). |
| [set_Id](./set_id/)(const System::String\&) | Sättare för [Aspose::Words::Markup::CustomXmlPart::get_Id](./get_id/). |
| static [Type](./type/)() |  |
## Anmärkningar


Ett DOCX- eller DOC-dokument kan innehålla en eller flera Custom XML Data Storage-delar. Aspose.Words bevarar och möjliggör att skapa och extrahera Custom XML Data via samlingen [CustomXmlParts](../../aspose.words/document/get_customxmlparts/).

## Exempel



Visar hur man skapar en strukturerad dokumenttagg med anpassad XML-data.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa en XML-del som innehåller data och lägg till den i dokumentets samling.
// Om vi aktiverar fliken "Developer" i Microsoft Word,
// kan vi hitta element från denna samling i "XML Mapping Pane", tillsammans med några standardelement.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Nedan finns två sätt att referera till XML-delar.
// 1 -  Genom ett index i den anpassade XML-delssamlingen:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  Genom GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Lägg till en XML-schemaassociation.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Klona en del och infoga den sedan i samlingen.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Iterera genom samlingen och skriv ut innehållet i varje del.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// Använd metoden "RemoveAt" för att ta bort den klonade delen med index.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Klona XML-delssamlingen och använd sedan metoden "Clear" för att ta bort alla dess element på en gång.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Skapa en strukturerad dokumenttagg som visar innehållet i vår del och infoga den i dokumentkroppen.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
