---
title: "Aspose::Words::Fields::DropDownItemCollection classe"
linktitle: "DropDownItemCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::DropDownItemCollection classe. Une collection de chaînes qui représentent tous les éléments d'un champ de formulaire déroulant. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


Une collection de chaînes qui représentent tous les éléments d'un champ de formulaire déroulant. Pour en savoir plus, consultez l'article de documentation [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::String\&) | Ajoute une chaîne à la fin de la collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Supprime tous les éléments de la collection. |
| [Contains](./contains/)(const System::String\&) | Détermine si la collection contient la valeur spécifiée. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient ou définit l'élément à l'index spécifié. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Obtient ou définit l'élément à l'index spécifié. |
| [IndexOf](./indexof/)(const System::String\&) | Renvoie l'index basé sur zéro de la valeur spécifiée dans la collection. |
| [Insert](./insert/)(int32_t, const System::String\&) | Insère une chaîne dans la collection à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Supprime la valeur spécifiée de la collection. |
| [RemoveAt](./removeat/)(int32_t) | Supprime une valeur à l'index spécifié. |
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

## Exemples



Montre comment insérer un champ de zone combinée et modifier les éléments de sa collection d'items.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une zone combinée, puis vérifiez sa collection d'éléments déroulants.
// Dans Microsoft Word, l'utilisateur cliquera sur la zone combinée,
// et choisira ensuite l'un des éléments de texte de la collection à afficher.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// Il existe deux façons d'ajouter un nouvel élément à une collection existante d'éléments de boîte déroulante.
// 1 -  Ajouter un élément à la fin de la collection :
dropDownItems->Add(u"Four");

// 2 -  Insérer un élément avant un autre élément à un index spécifié :
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Parcourez la collection et affichez chaque élément.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// Il existe deux façons de supprimer des éléments d'une collection d'éléments déroulants.
// 1 -  Supprimer un élément dont le contenu est égal à la chaîne transmise :
dropDownItems->Remove(u"Four");

// 2 -  Supprimer un élément à un index :
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Videz toute la collection d'éléments déroulants.
dropDownItems->Clear();
```

## Voir aussi

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
