---
title: "Aspose::Words::Markup::CustomXmlPart::get_Id‑metod"
linktitle: "get_Id"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomXmlPart::get_Id‑metod. Hämtar eller anger strängen som identifierar denna anpassade XML‑del i ett OOXML‑dokument i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.markup/customxmlpart/get_id/
---
## CustomXmlPart::get_Id method


Hämtar eller anger strängen som identifierar denna anpassade XML-del inom ett OOXML-dokument.

```cpp
System::String Aspose::Words::Markup::CustomXmlPart::get_Id() const
```

## Anmärkningar


ISO/IEC 29500 anger att detta värde är ett GUID, men äldre versioner av Microsoft Word tillät vilken sträng som helst här. Aspose.Words gör samma sak för ECMA-376-formatet. Observera dock att Microsoft Word Online misslyckas med att öppna ett dokument som skapats med ett icke-GUID‑värde. Så ett GUID är det föredragna värdet för denna egenskap.

Ett giltigt värde måste vara en identifierare som är unik bland alla anpassade XML‑datapart i detta dokument.

Standardvärdet är en tom sträng. Värdet kan inte vara **null**.

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

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
