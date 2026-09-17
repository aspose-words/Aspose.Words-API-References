---
title: "Aspose::Words::Markup::CustomPart::get_IsExternal méthode"
linktitle: "get_IsExternal"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::CustomPart::get_IsExternal méthode. False si cette partie personnalisée est stockée à l'intérieur du package OOXML. True si cette partie personnalisée est une cible externe en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.markup/custompart/get_isexternal/
---
## CustomPart::get_IsExternal method


False si cette partie personnalisée est stockée dans le package OOXML. True si cette partie personnalisée est une cible externe.

```cpp
bool Aspose::Words::Markup::CustomPart::get_IsExternal() const
```

## Remarques


La valeur par défaut est **false**.

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

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
