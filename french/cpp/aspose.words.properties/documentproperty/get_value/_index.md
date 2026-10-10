---
title: "Aspose::Words::Properties::DocumentProperty::get_Value méthode"
linktitle: "get_Value"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::DocumentProperty::get_Value méthode. Obtient ou définit la valeur de la propriété en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.properties/documentproperty/get_value/
---
## DocumentProperty::get_Value method


Obtient ou définit la valeur de la propriété.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Properties::DocumentProperty::get_Value()
```

## Remarques


Ne peut pas être **null**.

## Exemples



Montre comment travailler avec les propriétés de document intégrées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// L'objet "Document" contient une partie de ses métadonnées dans ses membres.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// Le document stocke également des métadonnées dans ses propriétés intégrées.
// Chaque propriété intégrée est un membre de l'objet "BuiltInDocumentProperties" du document.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Certaines propriétés peuvent contenir plusieurs valeurs.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## Voir aussi

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
