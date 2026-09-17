---
title: "Classe Aspose::Words::Markup::CustomPart"
linktitle: "CustomPart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Markup::CustomPart. Représente une partie personnalisée (contenu arbitraire) qui n'est pas définie par la norme ISO/IEC 29500. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.markup/custompart/
---
## CustomPart class


Représente une partie personnalisée (contenu arbitraire) qui n'est pas définie par la norme ISO/IEC 29500. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomPart : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Effectue une copie « suffisamment profonde » de l'objet. Ne duplique pas les octets de la valeur [Data](./get_data/). |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | Spécifie le type de contenu de cette partie personnalisée. |
| [get_Data](./get_data/)() const | Contient les données de cette partie personnalisée. |
| [get_IsExternal](./get_isexternal/)() const | False si cette partie personnalisée est stockée dans le package OOXML. True si cette partie personnalisée est une cible externe. |
| [get_Name](./get_name/)() const | Obtient ou définit le nom absolu de cette partie dans le package OOXML ou l'URL cible. |
| [get_RelationshipType](./get_relationshiptype/)() const | Obtient ou définit le type de relation du composant parent vers cette partie personnalisée. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Mutateur pour [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/). |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Mutateur pour [Aspose::Words::Markup::CustomPart::get_Data](./get_data/). |
| [set_IsExternal](./set_isexternal/)(bool) | Mutateur pour [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/). |
| [set_Name](./set_name/)(const System::String\&) | Mutateur pour [Aspose::Words::Markup::CustomPart::get_Name](./get_name/). |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | Mutateur pour [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/). |
| static [Type](./type/)() |  |
## Remarques


Cette classe représente une partie OOXML qui est la cible d'une « relation inconnue ». Toutes les relations non définies dans la norme ISO/IEC 29500 sont considérées comme des « relations inconnues ». Les relations inconnues sont autorisées dans un document Office Open XML à condition qu'elles respectent les directives de balisage des relations.

Microsoft Word conserve les parties personnalisées pendant les cycles d'ouverture/enregistrement. Des informations supplémentaires sont disponibles ici [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

Aspose.Words effectue également le round‑trip des parties personnalisées et, de plus, permet d'accéder programmatiquement à ces parties via les objets [CustomPart](./) et [CustomPartCollection](../custompartcollection/).

Ne confondez pas les parties personnalisées avec les données XML personnalisées. Utilisez [CustomXmlPart](../customxmlpart/) si vous devez accéder aux données XML personnalisées.

## Exemples



Montre comment accéder à la collection de parties personnalisées arbitraires d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Clonez la deuxième partie, puis ajoutez le clone à la collection.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Énumérez la collection et affichez chaque partie.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// Nous pouvons supprimer les éléments de cette collection individuellement, ou tous à la fois.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Voir aussi

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
