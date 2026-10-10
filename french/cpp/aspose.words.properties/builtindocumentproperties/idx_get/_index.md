---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get méthode"
linktitle: "idx_get"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get méthode. Retourne un objet DocumentProperty par le nom de la propriété en C++."
type: docs
weight: 35000
url: /fr/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


Retourne un objet [DocumentProperty](../../documentproperty/) par le nom de la propriété.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | System::String | Le nom de la propriété à récupérer, insensible à la casse. |
## Remarques


Les noms de chaîne des propriétés correspondent aux noms des propriétés typées disponibles depuis [BuiltInDocumentProperties](../).

Si vous demandez une propriété qui n'est pas présente dans le document, mais que le nom de la propriété est reconnu comme un nom intégré valide, un nouveau [DocumentProperty](../../documentproperty/) est créé, ajouté à la collection et retourné. La propriété nouvellement créée reçoit une valeur par défaut (chaîne vide, zéro, **false** ou DateTime.MinValue selon le type de la propriété intégrée).

Si vous demandez une propriété qui n'est pas présente dans le document et que le nom n'est pas reconnu comme un nom intégré, un **null** est retourné.

## Exemples



Montre comment travailler avec les propriétés de document personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Chaque document contient une collection de propriétés personnalisées qui, comme les propriétés intégrées, sont des paires clé-valeur.
// Le document possède une liste fixe de propriétés intégrées. L'utilisateur crée toutes les propriétés personnalisées.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
