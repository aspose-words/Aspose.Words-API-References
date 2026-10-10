---
title: "Aspose::Words::Markup::CustomXmlPartCollection::Clear metodo"
linktitle: "Cancella"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomXmlPartCollection::Clear metodo. Rimuove tutti gli elementi dalla raccolta in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.markup/customxmlpartcollection/clear/
---
## CustomXmlPartCollection::Clear method


Rimuove tutti gli elementi dalla collezione.

```cpp
void Aspose::Words::Markup::CustomXmlPartCollection::Clear()
```


## Esempi



Mostra come creare un tag di documento strutturato con dati XML personalizzati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Costruisci una parte XML che contiene dati e aggiungila alla collezione del documento.
// Se abiliti la scheda "Developer" in Microsoft Word,
// possiamo trovare gli elementi di questa collezione nel "Pannello di mappatura XML", insieme a pochi elementi predefiniti.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Di seguito sono due modi per fare riferimento alle parti XML.
// 1 -  Per indice nella collezione delle parti XML personalizzate:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  Per GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Aggiungi un'associazione di schema XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clona una parte, quindi inseriscila nella collezione.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Itera attraverso la collezione e stampa il contenuto di ogni parte.
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

// Usa il metodo "RemoveAt" per rimuovere la parte clonata per indice.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Clona la collezione delle parti XML, quindi usa il metodo "Clear" per rimuovere tutti i suoi elementi in una volta.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Crea un tag di documento strutturato che visualizzi il contenuto della nostra parte e inseriscilo nel corpo del documento.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## Vedi anche

* Class [CustomXmlPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
