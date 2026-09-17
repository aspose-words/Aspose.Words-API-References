---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping méthode"
linktitle: "get_XmlMapping"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping méthode. Obtient un objet qui représente le mappage de cette plage de balise de document structuré vers des données XML dans une partie XML personnalisée du document actuel en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


Obtient un objet qui représente le mappage de cette plage de balise de document structuré aux données XML d'une partie XML personnalisée du document actuel.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## Exemples



Montre comment définir les mappages XML pour le début de plage d'une balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// Construit une partie XML contenant du texte et l'ajoute à la collection CustomXmlPart du document.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Créez une balise de document structuré qui affichera le contenu de notre CustomXmlPart dans le document.
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// Si nous définissons un mappage pour notre balise de document structuré,
// elle n'affichera qu'une partie du CustomXmlPart vers laquelle pointe le XPath.
// Ce XPath pointera vers le deuxième élément "<text>" du premier élément "<root>" de notre CustomXmlPart.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## Voir aussi

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
