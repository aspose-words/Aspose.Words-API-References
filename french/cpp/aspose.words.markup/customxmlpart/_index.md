---
title: "Aspose::Words::Markup::CustomXmlPart class"
linktitle: "CustomXmlPart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::CustomXmlPart class. Représente une partie de stockage de données XML personnalisées (données XML personnalisées au sein d'un paquet). Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class


Représente une partie de stockage de données XML personnalisées (données XML personnalisées dans un package). Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPart : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Effectue une copie « suffisamment profonde » de l'objet. Ne duplique pas les octets de la valeur [Data](./get_data/). |
| [CustomXmlPart](./customxmlpart/)() |  |
| [get_Data](./get_data/)() const | Obtient ou définit le contenu XML de cette partie de stockage de données XML personnalisées. |
| [get_DataChecksum](./get_datachecksum/)() | Spécifie une somme de contrôle de redondance cyclique (CRC) du contenu [Data](./get_data/). |
| [get_Id](./get_id/)() const | Obtient ou définit la chaîne qui identifie cette partie XML personnalisée dans un document OOXML. |
| [get_Schemas](./get_schemas/)() const | Spécifie l'ensemble des schémas XML associés à cette partie XML personnalisée. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Définisseur pour [Aspose::Words::Markup::CustomXmlPart::get_Data](./get_data/). |
| [set_Id](./set_id/)(const System::String\&) | Définisseur pour [Aspose::Words::Markup::CustomXmlPart::get_Id](./get_id/). |
| static [Type](./type/)() |  |
## Remarques


Un document DOCX ou DOC peut contenir une ou plusieurs parties de stockage de données XML personnalisées. Aspose.Words préserve et permet de créer et d'extraire des données XML personnalisées via la collection [CustomXmlParts](../../aspose.words/document/get_customxmlparts/).

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
