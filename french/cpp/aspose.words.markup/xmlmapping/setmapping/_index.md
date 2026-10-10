---
title: "Méthode Aspose::Words::Markup::XmlMapping::SetMapping"
linktitle: "SetMapping"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Markup::XmlMapping::SetMapping. Définit un mappage entre le tag de document structuré parent et un nœud XML d'une partie de données XML personnalisée en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.markup/xmlmapping/setmapping/
---
## XmlMapping::SetMapping method


Définit une correspondance entre la balise de document structuré parent et un nœud XML d'une partie de données XML personnalisée.

```cpp
bool Aspose::Words::Markup::XmlMapping::SetMapping(const System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> &customXmlPart, const System::String &xPath, const System::String &prefixMapping)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| customXmlPart | const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\& | Une partie de données XML personnalisée vers laquelle mapper. |
| xPath | const System::String\& | Une expression XPath pour trouver le nœud XML. |
| prefixMapping | const System::String\& | Mappages de préfixes d'espace de noms XML pour évaluer le XPath. |

### ReturnValue

Un indicateur indiquant si le tag de document structuré parent est correctement mappé au nœud XML.

## Exemples



Montre comment créer une balise de document structuré avec des données XML personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Construisez une partie XML contenant des données et ajoutez‑la à la collection du document.
// Si nous activons l’onglet « Developer » dans Microsoft Word,
// nous pouvons trouver les éléments de cette collection dans le « XML Mapping Pane », ainsi que quelques éléments par défaut.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Voici deux façons de référencer les parties XML.
// 1 -  Par un indice dans la collection de parties XML personnalisées :
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  Par GUID :
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Ajoutez une association de schéma XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clonez une partie, puis insérez‑la dans la collection.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Parcourez la collection et affichez le contenu de chaque partie.
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

// Utilisez la méthode « RemoveAt » pour supprimer la partie clonée par indice.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Clonez la collection de parties XML, puis utilisez la méthode « Clear » pour supprimer tous ses éléments d’un coup.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Créez une balise de document structuré qui affichera le contenu de notre partie et insérez‑la dans le corps du document.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## Voir aussi

* Class [CustomXmlPart](../../customxmlpart/)
* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
