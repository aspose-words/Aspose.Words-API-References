---
title: "Aspose::Words::Markup::SdtListItemCollection class"
linktitle: "SdtListItemCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::SdtListItemCollection class. Fournit l'accès aux éléments SdtListItem d'une balise de document structuré. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class


Fournit l'accès aux éléments [SdtListItem](../sdtlistitem/) d'une balise de document structuré. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class SdtListItemCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Ajoute un élément à cette collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Efface tous les éléments de cette collection. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d'éléments dans la collection. |
| [get_SelectedValue](./get_selectedvalue/)() | Spécifie la valeur actuellement sélectionnée dans cette liste. Valeur nulle autorisée, ce qui signifie qu'aucune entrée actuellement sélectionnée n'est associée à cette collection d'éléments de liste. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie un objet [SdtListItem](../sdtlistitem/) donné son indice basé sur zéro dans la collection. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Supprime un élément de liste à l'indice spécifié. |
| [set_SelectedValue](./set_selectedvalue/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Mutateur pour [Aspose::Words::Markup::SdtListItemCollection::get_SelectedValue](./get_selectedvalue/). |
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



Montre comment travailler avec les balises de document structuré de type liste déroulante.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Une balise de document structuré de type liste déroulante est un formulaire qui permet à l'utilisateur de
// sélectionner une option dans une liste en cliquant avec le bouton gauche et en ouvrant le formulaire dans Microsoft Word.
// La propriété "ListItems" contient tous les éléments de liste, et chaque élément de liste est un "SdtListItem".
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// Ajoutez 3 éléments de liste supplémentaires. Initialisez ces éléments en utilisant un constructeur différent de celui du premier élément
// pour afficher des chaînes différentes de leurs valeurs.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// La liste déroulante affiche le premier élément. Assignez un autre élément de liste à la "SelectedValue" pour l'afficher.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Énumérez la collection et imprimez chaque élément.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// Supprimez le dernier élément de la liste.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Comme notre contrôle déroulant est configuré pour afficher l'élément supprimé par défaut, fournissez-lui un élément à afficher qui existe.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// Utilisez la méthode "Clear" pour vider toute la collection d'éléments de la liste déroulante en une seule fois.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## Voir aussi

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
