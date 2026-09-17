---
title: "Aspose::Words::Markup::CustomXmlPartCollection classe"
linktitle: "CustomXmlPartCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::CustomXmlPartCollection classe. Représente une collection de parties XML personnalisées. Les éléments sont des objets CustomXmlPart. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class


Représente une collection de parties XML personnalisées. Les éléments sont des objets [CustomXmlPart](../customxmlpart/). Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPartCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Ajoute un élément à la collection. |
| [Add](./add/)(const System::String\&, const System::String\&) | Crée une nouvelle partie XML avec le XML spécifié et l'ajoute à la collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Supprime tous les éléments de la collection. |
| [Clone](./clone/)() | Effectue une copie profonde de cette collection et de ses éléments. |
| [CustomXmlPartCollection](./customxmlpartcollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [GetById](./getbyid/)(const System::String\&) | Recherche et renvoie une partie XML personnalisée par son identifiant. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient ou définit un élément à l'index spécifié. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Obtient ou définit un élément à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Supprime un élément à l'index spécifié. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Remarques


Vous n'avez généralement pas besoin de créer des instances de cette classe. Vous pouvez accéder aux données XML personnalisées stockées dans un document via la propriété [CustomXmlParts](../../aspose.words/document/get_customxmlparts/).

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
