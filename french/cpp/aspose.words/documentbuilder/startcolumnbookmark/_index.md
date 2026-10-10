---
title: "Aspose::Words::DocumentBuilder::StartColumnBookmark méthode"
linktitle: "StartColumnBookmark"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::StartColumnBookmark méthode. Marque la position actuelle dans le document comme le début d'un signet de colonne. La position doit être dans une cellule de tableau en C++."
type: docs
weight: 69000
url: /fr/cpp/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder::StartColumnBookmark method


Marque la position actuelle dans le document comme le début d'un signet de colonne. La position doit être dans une cellule de tableau.

```cpp
System::SharedPtr<Aspose::Words::BookmarkStart> Aspose::Words::DocumentBuilder::StartColumnBookmark(const System::String &bookmarkName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nom du signet. |

### ReturnValue

Le nœud de début de signet qui vient d'être créé.
## Remarques


Un signet de colonne couvre une ou plusieurs colonnes dans une plage de lignes. Pour créer un signet valide, vous devez appeler à la fois [StartColumnBookmark()](../) et [EndColumnBookmark()](../) avec le même paramètre *bookmarkName*.

Les signets mal formés ou les signets avec des noms en double seront ignorés lors de l'enregistrement du document.

La position réelle du nœud [BookmarkStart](../../bookmarkstart/) inséré peut différer de la position actuelle du constructeur de document.

## Exemples



Montre comment créer un signet de colonne.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

builder->InsertCell();
// Les cellules 1,2,4,5 seront marquées d'un signet.
builder->StartColumnBookmark(u"MyBookmark_1");
// Les signets mal formés ou les signets avec des noms en double seront ignorés lors de l'enregistrement du document.
builder->StartColumnBookmark(u"MyBookmark_1");
builder->StartColumnBookmark(u"BadStartBookmark");
builder->Write(u"Cell 1");

builder->InsertCell();
builder->Write(u"Cell 2");

builder->InsertCell();
builder->Write(u"Cell 3");

builder->EndRow();

builder->InsertCell();
builder->Write(u"Cell 4");

builder->InsertCell();
builder->Write(u"Cell 5");
builder->EndColumnBookmark(u"MyBookmark_1");
builder->EndColumnBookmark(u"MyBookmark_1");

ASSERT_THROW(static_cast<std::function<void()>>([&builder]() -> void
{
    builder->EndColumnBookmark(u"BadEndBookmark");

builder->InsertCell();
builder->Write(u"Cell 6");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"Bookmarks.CreateColumnBookmark.docx");
```

## Voir aussi

* Class [BookmarkStart](../../bookmarkstart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
