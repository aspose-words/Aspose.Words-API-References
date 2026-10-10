---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping method"
linktitle: "get_XmlMapping"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping. Restituisce un oggetto che rappresenta la mappatura di questo intervallo di tag di documento strutturato ai dati XML in una parte XML personalizzata del documento corrente in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


Restituisce un oggetto che rappresenta la mappatura di questo intervallo di tag di documento strutturato ai dati XML in una parte XML personalizzata del documento corrente.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## Esempi



Mostra come impostare le mappature XML per l'inizio dell'intervallo di un tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// Crea una parte XML che contiene testo e aggiungila alla collezione CustomXmlPart del documento.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Crea un tag di documento strutturato che visualizzerà il contenuto del nostro CustomXmlPart nel documento.
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// Se impostiamo una mappatura per il nostro tag di documento strutturato,
// visualizzerà solo una parte del CustomXmlPart a cui punta l'XPath.
// Questo XPath punterà al secondo elemento "<text>" del contenuto del primo elemento "<root>" del nostro CustomXmlPart.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## Vedi anche

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
