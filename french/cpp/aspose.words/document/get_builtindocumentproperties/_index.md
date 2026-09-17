---
title: "Aspose::Words::Document::get_BuiltInDocumentProperties méthode"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_BuiltInDocumentProperties méthode. Retourne une collection qui représente toutes les propriétés intégrées du document en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words/document/get_builtindocumentproperties/
---
## Document::get_BuiltInDocumentProperties method


Renvoie une collection qui représente toutes les propriétés intégrées du document.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::Document::get_BuiltInDocumentProperties() const
```


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

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
