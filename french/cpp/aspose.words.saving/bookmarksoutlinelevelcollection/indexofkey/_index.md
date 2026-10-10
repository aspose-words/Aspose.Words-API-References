---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::IndexOfKey méthode"
linktitle: "IndexOfKey"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::IndexOfKey méthode. Retourne l'index basé sur zéro du signet spécifié dans la collection en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/
---
## BookmarksOutlineLevelCollection::IndexOfKey method


Renvoie l'index basé sur zéro du signet spécifié dans la collection.

```cpp
int32_t Aspose::Words::Saving::BookmarksOutlineLevelCollection::IndexOfKey(const System::String &name)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| name | const System::String\& | Le nom du signet insensible à la casse. |

### ReturnValue

L'index basé sur zéro. Valeur négative si non trouvé.

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

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
