---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection classe"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection classe. Une collection de niveaux de contour de signets individuels. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class


Une collection de niveaux de plan pour les signets individuels. Pour en savoir plus, consultez l'article de documentation [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarksOutlineLevelCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, int32_t>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](./add/)(const System::String\&, int32_t) | Ajoute un signet à la collection. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/)() |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Supprime tous les éléments de la collection. |
| [Contains](./contains/)(const System::String\&) | Détermine si la collection contient un signet portant le nom donné. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtient le nombre d’éléments contenus dans la collection. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur qui peut être utilisé pour parcourir tous les éléments de la collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Obtient ou définit le niveau de contour d'un signet par son nom. |
| [idx_get](./idx_get/)(int32_t) | Obtient ou définit le niveau de contour d'un signet à l'index spécifié. |
| [idx_set](./idx_set/)(const System::String\&, int32_t) | Obtient ou définit le niveau de contour d'un signet par son nom. |
| [idx_set](./idx_set/)(int32_t, int32_t) | Obtient ou définit le niveau de contour d'un signet à l'index spécifié. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Renvoie l'index basé sur zéro du signet spécifié dans la collection. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Supprime un signet portant le nom spécifié de la collection. |
| [RemoveAt](./removeat/)(int32_t) | Supprime un signet à l'index spécifié. |
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


La clé est un nom de signet sous forme de chaîne insensible à la casse. La valeur est un entier représentant le niveau de contour du signet.

[Bookmark](../../aspose.words/bookmark/) outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.

## Exemples



Montre comment définir les niveaux de contour pour les signets.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insère un signet avec un autre signet imbriqué à l'intérieur.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// Insère un autre signet.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// Lors de l'enregistrement au format .pdf, les signets peuvent être accessibles via un menu déroulant et utilisés comme ancres par la plupart des lecteurs.
// Les signets peuvent également avoir des valeurs numériques pour les niveaux de plan,
// permettant aux entrées de plan de niveau inférieur de masquer les entrées enfants de niveau supérieur lorsqu'elles sont réduites dans le lecteur.
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// Nous pouvons supprimer deux éléments afin qu'il ne reste que la désignation du niveau de plan pour "Bookmark 1".
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// Il y a neuf niveaux de plan. Leur numérotation sera optimisée pendant l'opération d'enregistrement.
// Dans ce cas, les niveaux "5" et "9" deviendront "2" et "3".
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Vider cette collection préservera les signets et les placera tous au même niveau de plan.
outlineLevels->Clear();
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
