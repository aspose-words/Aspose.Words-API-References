---
title: "Aspose::Words::Markup::XmlMapping classe"
linktitle: "XmlMapping"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::XmlMapping classe. Spécifie les informations utilisées pour établir une correspondance entre la balise de document structuré parent et un élément XML stocké dans une partie de données XML personnalisée du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


Spécifie les informations utilisées pour établir une correspondance entre la balise de document structuré parent et un élément XML stocké dans une partie de données XML personnalisée du document. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class XmlMapping : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Delete](./delete/)() | Supprime la correspondance du document structuré parent avec les données XML. |
| [get_CustomXmlPart](./get_customxmlpart/)() | Renvoie la partie de données XML personnalisée à laquelle la balise de document structuré parent est mappée. |
| [get_IsMapped](./get_ismapped/)() | Renvoie **true** si la balise de document structuré parent est correctement mappée aux données XML. |
| [get_PrefixMappings](./get_prefixmappings/)() const | Renvoie les correspondances de préfixes d'espaces de noms XML pour évaluer le [XPath](./get_xpath/). |
| [get_StoreItemId](./get_storeitemid/)() | Spécifie l'identifiant de données XML personnalisé pour la partie de données XML personnalisée qui sera utilisée pour évaluer l'expression [XPath](./get_xpath/). |
| [get_XPath](./get_xpath/)() const | Renvoie l'expression XPath, qui est évaluée pour trouver le nœud XML personnalisé mappé à la balise de document structuré parent. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | Définit une correspondance entre la balise de document structuré parent et un nœud XML d'une partie de données XML personnalisée. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
