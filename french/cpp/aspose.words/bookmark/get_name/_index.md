---
title: "Aspose::Words::Bookmark::get_Name méthode"
linktitle: "get_Name"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Bookmark::get_Name méthode. Obtient ou définit le nom du signet en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


Obtient ou définit le nom du signet.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## Exemples



Montre comment insérer un signet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un signet valide possède un nom, un nœud BookmarkStart et un nœud BookmarkEnd.
// Tout espace blanc dans les noms des signets sera converti en tirets bas si nous ouvrons le document enregistré avec Microsoft Word.
// Si nous mettons en surbrillance le nom du signet dans Microsoft Word via Insertion -> Liens -> Signet, et appuyons sur "Go To",
// le curseur sautera vers le texte compris entre les nœuds BookmarkStart et BookmarkEnd.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// Les signets sont stockés dans cette collection.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## Voir aussi

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
