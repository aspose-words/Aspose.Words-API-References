---
title: "Aspose::Words::VariableCollection classe"
linktitle: "VariableCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::VariableCollection classe. Une collection de variables de document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 73000
url: /fr/cpp/aspose.words/variablecollection/
---
## VariableCollection class


Une collection de variables de document. Pour en savoir plus, consultez l'article de documentation [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class VariableCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, System::String>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Ajoute une variable de document à la collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Supprime tous les éléments de la collection. |
| [Contains](./contains/)(const System::String\&) | Détermine si la collection contient une variable de document avec le nom donné. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir toutes les variables de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtient ou définit une variable de document par son nom insensible à la casse. Les valeurs **null** ne sont pas autorisées comme côté droit de l'affectation et seront remplacées par une chaîne vide. |
| [idx_get](./idx_get/)(int32_t) | Obtient ou définit une variable de document à l'index spécifié. Les valeurs **null** ne sont pas autorisées comme côté droit de l'affectation et seront remplacées par une chaîne vide. |
| [idx_set](./idx_set/)(const System::String\&, const System::String\&) | Obtient ou définit une variable de document par son nom insensible à la casse. Les valeurs **null** ne sont pas autorisées comme côté droit de l'affectation et seront remplacées par une chaîne vide. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Obtient ou définit une variable de document à l'index spécifié. Les valeurs **null** ne sont pas autorisées comme côté droit de l'affectation et seront remplacées par une chaîne vide. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Renvoie l'index basé sur zéro de la variable de document spécifiée dans la collection. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Supprime une variable de document avec le nom spécifié de la collection. |
| [RemoveAt](./removeat/)(int32_t) | Supprime une variable de document à l'index spécifié. |
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


Les noms et valeurs des variables sont des chaînes.

Les noms de variables sont insensibles à la casse.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
