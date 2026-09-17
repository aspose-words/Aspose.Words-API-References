---
title: "Méthode Aspose::Words::Properties::DocumentPropertyCollection::GetEnumerator"
linktitle: "GetEnumerator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Properties::DocumentPropertyCollection::GetEnumerator. Retourne un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.properties/documentpropertycollection/getenumerator/
---
## DocumentPropertyCollection::GetEnumerator method


Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> Aspose::Words::Properties::DocumentPropertyCollection::GetEnumerator() override
```


## Exemples



Montre comment travailler avec les propriétés personnalisées d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Les propriétés personnalisées du document sont des paires clé-valeur que nous pouvons ajouter au document.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// La collection trie les propriétés personnalisées par ordre alphabétique.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Imprime chaque propriété personnalisée du document.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Affiche la valeur d'une propriété personnalisée à l'aide d'un champ DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Nous pouvons trouver ces propriétés personnalisées dans Microsoft Word via "Fichier" -> "Propriétés" > "Propriétés avancées" > "Personnalisées".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Voici trois façons de supprimer les propriétés personnalisées d'un document.
// 1 -  Supprimer par indice :
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Supprimer par nom:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Vider la collection entière d'un coup:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Voir aussi

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
