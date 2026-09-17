---
title: "Aspose::Words::VariableCollection::Remove méthode"
linktitle: "Supprimer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::VariableCollection::Remove méthode. Supprime une variable de document avec le nom spécifié de la collection en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words/variablecollection/remove/
---
## VariableCollection::Remove method


Supprime une variable de document avec le nom spécifié de la collection.

```cpp
void Aspose::Words::VariableCollection::Remove(const System::String &name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom insensible à la casse de la variable. |

## Exemples



Montre comment travailler avec la collection de variables d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::VariableCollection> variables = doc->get_Variables();

// Chaque document possède une collection de variables sous forme de paires clé/valeur, à laquelle nous pouvons ajouter des éléments.
variables->Add(u"Home address", u"123 Main St.");
variables->Add(u"City", u"London");
variables->Add(u"Bedrooms", u"3");

ASSERT_EQ(3, variables->get_Count());

// Nous pouvons afficher les valeurs des variables dans le corps du document en utilisant les champs DOCVARIABLE.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
field->set_VariableName(u"Home address");
field->Update();

ASSERT_EQ(u"123 Main St.", field->get_Result());

// Attribuer des valeurs aux clés existantes les mettra à jour.
variables->Add(u"Home address", u"456 Queen St.");

// Nous devrons ensuite mettre à jour les champs DOCVARIABLE pour garantir qu'ils affichent une valeur à jour.
ASSERT_EQ(u"123 Main St.", field->get_Result());

field->Update();

ASSERT_EQ(u"456 Queen St.", field->get_Result());

// Vérifiez que les variables de document avec un certain nom ou une certaine valeur existent.
ASSERT_TRUE(variables->Contains(u"City"));
ASSERT_TRUE(variables->LINQ_Any(static_cast<System::Func<System::Collections::Generic::KeyValuePair<System::String, System::String>, bool>>(static_cast<std::function<bool(System::Collections::Generic::KeyValuePair<System::String, System::String> v)>>([](System::Collections::Generic::KeyValuePair<System::String, System::String> v) -> bool
{
    return v.get_Value() == u"London";
}))));

// La collection de variables trie automatiquement les variables par ordre alphabétique du nom.
ASSERT_EQ(0, variables->IndexOfKey(u"Bedrooms"));
ASSERT_EQ(1, variables->IndexOfKey(u"City"));
ASSERT_EQ(2, variables->IndexOfKey(u"Home address"));

ASSERT_EQ(u"3", variables->idx_get(0));
ASSERT_EQ(u"London", variables->idx_get(u"City"));

// Énumérez la collection de variables.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::Collections::Generic::KeyValuePair<System::String, System::String>>> enumerator = doc->get_Variables()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: {0}, Value: {1}", enumerator->get_Current().get_Key(), enumerator->get_Current().get_Value()) << std::endl;
    }
}

// Voici trois façons de supprimer des variables de document d'une collection.
// 1 -  Par nom :
variables->Remove(u"City");

ASSERT_FALSE(variables->Contains(u"City"));

// 2 -  Par indice :
variables->RemoveAt(1);

ASSERT_FALSE(variables->Contains(u"Home address"));

// 3 -  Vider la collection entière d'un coup :
variables->Clear();

ASSERT_EQ(0, variables->get_Count());
```

## Voir aussi

* Class [VariableCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
