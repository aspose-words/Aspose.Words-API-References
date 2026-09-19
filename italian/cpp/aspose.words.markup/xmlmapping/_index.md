---
title: "Aspose::Words::Markup::XmlMapping classe"
linktitle: "XmlMapping"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::XmlMapping classe. Specifica le informazioni utilizzate per stabilire una mappatura tra il tag di documento strutturato padre e un elemento XML memorizzato all'interno di una parte di dati XML personalizzata nel documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


Specifica le informazioni utilizzate per stabilire una mappatura tra il tag di documento strutturato padre e un elemento XML memorizzato all'interno di una parte di dati XML personalizzata nel documento. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class XmlMapping : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Delete](./delete/)() | Elimina la mappatura del documento strutturato padre ai dati XML. |
| [get_CustomXmlPart](./get_customxmlpart/)() | Restituisce la parte di dati XML personalizzata a cui è mappato il tag di documento strutturato padre. |
| [get_IsMapped](./get_ismapped/)() | Restituisce **true** se il tag di documento strutturato padre è stato mappato con successo ai dati XML. |
| [get_PrefixMappings](./get_prefixmappings/)() const | Restituisce le mappature dei prefissi degli spazi dei nomi XML per valutare l'[XPath](./get_xpath/). |
| [get_StoreItemId](./get_storeitemid/)() | Specifica l'identificatore dei dati XML personalizzati per la parte di dati XML personalizzata che sarà utilizzata per valutare l'espressione [XPath](./get_xpath/). |
| [get_XPath](./get_xpath/)() const | Restituisce l'espressione XPath, che viene valutata per trovare il nodo XML personalizzato mappato al tag di documento strutturato padre. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | Imposta una mappatura tra il tag di documento strutturato padre e un nodo XML di una parte di dati XML personalizzata. |
| static [Type](./type/)() |  |

## Esempi



Mostra come impostare le mappature XML per le parti XML personalizzate.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea una parte XML che contiene testo e aggiungila alla collezione CustomXmlPart del documento.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Crea un tag di documento strutturato che visualizzerà il contenuto del nostro CustomXmlPart.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// Imposta una mappatura per il nostro tag di documento strutturato. Questa mappatura istruirà
// il nostro tag di documento strutturato a visualizzare una porzione del contenuto testuale della parte XML a cui punta l'XPath.
// In questo caso, sarà il contenuto del secondo elemento "<text>" del primo elemento "<root>": "Text element #2".
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// Aggiungi il tag di documento strutturato al documento per visualizzare il contenuto della nostra parte personalizzata.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
