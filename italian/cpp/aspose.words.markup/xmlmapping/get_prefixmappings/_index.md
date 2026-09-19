---
title: "Aspose::Words::Markup::XmlMapping::get_PrefixMappings metodo"
linktitle: "get_PrefixMappings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::XmlMapping::get_PrefixMappings metodo. Restituisce le mappature dei prefissi di spazio dei nomi XML per valutare l'XPath in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.markup/xmlmapping/get_prefixmappings/
---
## XmlMapping::get_PrefixMappings method


Restituisce le mappature dei prefissi di spazio dei nomi XML per valutare l'[XPath](../get_xpath/).

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_PrefixMappings() const
```


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

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
