---
title: "Aspose::Words::Lists::ListCollection class"
linktitle: "ListCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Lists::ListCollection class. Stocke et gère le formatage des listes à puces et numérotées utilisées dans un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.lists/listcollection/
---
## ListCollection class


Stocke et gère le formatage des listes à puces et numérotées utilisées dans un document. Pour en savoir plus, consultez l’article de documentation [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(Aspose::Words::Lists::ListTemplate) | Crée une nouvelle liste basée sur un modèle prédéfini et l'ajoute à la collection de listes du document. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Crée une nouvelle liste qui fait référence à un style de liste et l'ajoute à la collection de listes du document. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Crée une nouvelle liste en copiant la liste spécifiée et l'ajoute à la collection de listes du document. |
| [AddSingleLevelList](./addsinglelevellist/)(Aspose::Words::Lists::ListTemplate) | Crée une nouvelle liste à un seul niveau basée sur le modèle prédéfini et l'ajoute à la collection de listes du document. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre de listes numérotées et à puces dans le document. |
| [get_Document](./get_document/)() const | Obtient le document propriétaire. |
| [GetEnumerator](./getenumerator/)() override | Obtient l'objet énumérateur qui énumérera les listes dans le document. |
| [GetListByListId](./getlistbylistid/)(int32_t) | Obtient une liste par son identifiant de liste. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtient une liste par indice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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


Une liste dans un document Microsoft Word est un ensemble de propriétés de mise en forme de liste. La mise en forme des listes est stockée dans la collection [ListCollection](./) séparément des paragraphes de texte.

Vous ne créez pas d'objets de cette classe. Il n'existe toujours qu'un seul objet [ListCollection](./) par document et il est accessible via la propriété [Lists](../../aspose.words/documentbase/get_lists/).

Pour créer une nouvelle liste basée sur un modèle de liste prédéfini ou sur un style de liste, utilisez la méthode [Add()](../).

Pour créer une nouvelle liste avec une mise en forme identique à une liste existante, utilisez la méthode [AddCopy()](../).

Pour rendre un paragraphe à puces ou numéroté, vous devez appliquer la mise en forme de liste à un paragraphe en assignant un objet [List](../list/) à la propriété [List](../listformat/get_list/) de [ListFormat](../listformat/).

Pour supprimer la mise en forme de liste d'un paragraphe, utilisez la méthode [RemoveNumbers](../listformat/removenumbers/).

Si vous connaissez un peu le WordprocessingML, vous savez peut‑être qu’il définit des concepts séparés pour « list » et « list definition ». Cela correspond exactement à la façon dont la mise en forme des listes est stockée dans un document Microsoft Word au niveau bas. La définition [List](../list/) est comme un « schéma » et la liste est comme une instance d’une définition de liste.

Pour simplifier le modèle de programmation, Aspose.Words masque la distinction entre liste et définition de liste de la même manière que Microsoft Word le fait dans son interface utilisateur. Cela vous permet de vous concentrer davantage sur l’apparence souhaitée de votre document, plutôt que de créer des objets de bas niveau pour satisfaire les exigences du format de fichier Microsoft Word.

Il n’est pas possible de supprimer les listes une fois créées dans la version actuelle de [Aspose.Words](../../aspose.words/). Cela est similaire à Microsoft Word où l'utilisateur n’a pas de contrôle explicite sur les définitions de listes.

## Exemples



Montre comment travailler avec les niveaux de listes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Voici deux types de listes que nous pouvons créer à l'aide d'un constructeur de document.
// 1 -  Une liste numérotée :
// Les listes numérotées créent un ordre logique pour leurs paragraphes en numérotant chaque élément.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// En définissant la propriété "ListLevelNumber", nous pouvons augmenter le niveau de la liste
// pour commencer une sous‑liste autonome à l'élément de liste actuel.
// Le modèle de liste Microsoft Word appelé "NumberDefault" utilise des chiffres pour créer des niveaux de liste pour le premier niveau de liste.
// Les niveaux de liste plus profonds utilisent des lettres et des chiffres romains minuscules.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Une liste à puces :
// Cette liste appliquera une indentation et un symbole de puce ("•") avant chaque paragraphe.
// Les niveaux plus profonds de cette liste utiliseront des symboles différents, tels que "■" et "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Nous pouvons désactiver le formatage de liste pour ne pas formater les paragraphes suivants comme des listes en désactivant le drapeau "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


Montre comment redémarrer la numérotation dans une liste en copiant une liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste à partir d'un modèle Microsoft Word et personnalisez son premier niveau de liste.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Appliquez notre liste à certains paragraphes.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Nous pouvons ajouter une copie d'une liste existante à la collection de listes du document
// pour créer une liste similaire sans modifier l'original.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Appliquez la deuxième liste aux nouveaux paragraphes.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
