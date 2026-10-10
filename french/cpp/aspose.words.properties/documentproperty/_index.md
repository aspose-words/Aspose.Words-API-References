---
title: "Aspose::Words::Properties::DocumentProperty classe"
linktitle: "DocumentProperty"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::DocumentProperty classe. Représente une propriété de document personnalisée ou intégrée. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


Représente une propriété de document personnalisée ou intégrée. Pour en savoir plus, consultez l’article de documentation [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentProperty : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | Indique si cette propriété est liée au contenu ou non. |
| [get_LinkSource](./get_linksource/)() const | Obtient la source d'une propriété de document personnalisée liée. |
| [get_Name](./get_name/)() const | Renvoie le nom de la propriété. |
| [get_Type](./get_type/)() const | Obtient le type de données de la propriété. |
| [get_Value](./get_value/)() | Obtient ou définit la valeur de la propriété. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | Définisseur pour [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | Renvoie la valeur de la propriété en tant que bool. |
| [ToByteArray](./tobytearray/)() | Renvoie la valeur de la propriété sous forme de tableau d'octets. |
| [ToDateTime](./todatetime/)() | Renvoie la valeur de la propriété en tant que **DateTime** en UTC. |
| [ToDouble](./todouble/)() | Renvoie la valeur de la propriété en tant que double. |
| [ToInt](./toint/)() | Renvoie la valeur de la propriété en tant qu'entier. |
| [ToString](./tostring/)() const override | Renvoie la valeur de la propriété sous forme de chaîne formatée selon la locale actuelle. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
