---
title: "Méthode Aspose::Words::Markup::XmlMapping::get_CustomXmlPart"
linktitle: "get_CustomXmlPart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Markup::XmlMapping::get_CustomXmlPart. Retourne la partie de données XML personnalisée à laquelle le tag de document structuré parent est mappé en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.markup/xmlmapping/get_customxmlpart/
---
## XmlMapping::get_CustomXmlPart method


Renvoie la partie de données XML personnalisée à laquelle la balise de document structuré parent est mappée.

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> Aspose::Words::Markup::XmlMapping::get_CustomXmlPart()
```


## Exemples



Montre comment définir des correspondances XML pour les parties XML personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Construit une partie XML contenant du texte et l'ajoute à la collection CustomXmlPart du document.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Crée une balise de document structuré qui affichera le contenu de notre CustomXmlPart.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// Définissez une correspondance pour notre balise de document structuré. Cette correspondance indiquera
// à notre balise de document structuré d'afficher une partie du texte de la partie XML vers laquelle pointe le XPath.
// Dans ce cas, il s'agira du contenu du deuxième élément "<text>" du premier élément "<root>": "Text element #2".
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// Ajoutez la balise de document structuré au document pour afficher le contenu de notre partie personnalisée.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## Voir aussi

* Class [CustomXmlPart](../../customxmlpart/)
* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
