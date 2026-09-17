---
title: "Aspose::Words::Document::get_PackageCustomParts méthode"
linktitle: "get_PackageCustomParts"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_PackageCustomParts méthode. Obtient ou définit la collection de parties personnalisées (contenu arbitraire) qui sont liées au package OOXML en utilisant les « relations inconnues » en C++."
type: docs
weight: 42000
url: /fr/cpp/aspose.words/document/get_packagecustomparts/
---
## Document::get_PackageCustomParts method


Obtient ou définit la collection de parties personnalisées (contenu arbitraire) qui sont liées au package OOXML à l'aide de « relations inconnues ».

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomPartCollection> Aspose::Words::Document::get_PackageCustomParts() const
```

## Remarques


Ne confondez pas ces parties personnalisées avec les données Custom XML. Si vous devez accéder aux parties Custom XML, utilisez la propriété [CustomXmlParts](../get_customxmlparts/).

Cette collection contient des parties OOXML dont le parent est le package OOXML et dont les cibles sont d'une « relation inconnue ». Pour plus d'informations, voir [CustomPart](../../../aspose.words.markup/custompart/).

Aspose.Words charge et enregistre uniquement des parties personnalisées dans les documents OOXML.

Cette propriété ne peut pas être **null**.

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

* Class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
