---
title: "Aspose::Words::Markup::CustomXmlPart class"
linktitle: "CustomXmlPart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomXmlPart class. Rappresenta una parte di archiviazione dati XML personalizzata (dati XML personalizzati all'interno di un pacchetto). Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class


Rappresenta una parte di archiviazione dati XML personalizzata (dati XML personalizzati all'interno di un pacchetto). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPart : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clone](./clone/)() | Crea una copia "deep enough" dell'oggetto. Non duplica i byte del valore [Data](./get_data/). |
| [CustomXmlPart](./customxmlpart/)() |  |
| [get_Data](./get_data/)() const | Ottiene o imposta il contenuto XML di questa parte di archiviazione dati XML personalizzata. |
| [get_DataChecksum](./get_datachecksum/)() | Specifica un checksum di controllo di ridondanza ciclica (CRC) del contenuto [Data](./get_data/). |
| [get_Id](./get_id/)() const | Ottiene o imposta la stringa che identifica questa parte XML personalizzata all'interno di un documento OOXML. |
| [get_Schemas](./get_schemas/)() const | Specifica l'insieme di schemi XML associati a questa parte XML personalizzata. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Setter per [Aspose::Words::Markup::CustomXmlPart::get_Data](./get_data/). |
| [set_Id](./set_id/)(const System::String\&) | Setter per [Aspose::Words::Markup::CustomXmlPart::get_Id](./get_id/). |
| static [Type](./type/)() |  |
## Note


Un documento DOCX o DOC può contenere una o più parti di archiviazione dati XML personalizzati. Aspose.Words preserva e consente di creare ed estrarre dati XML personalizzati tramite la collezione [CustomXmlParts](../../aspose.words/document/get_customxmlparts/).

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
