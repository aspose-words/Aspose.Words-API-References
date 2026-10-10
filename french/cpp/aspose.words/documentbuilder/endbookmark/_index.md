---
title: "Aspose::Words::DocumentBuilder::EndBookmark method"
linktitle: "EndBookmark"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::EndBookmark method. Marque la position actuelle dans le document comme la fin d'un signet en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder::EndBookmark method


Marque la position actuelle dans le document comme la fin d'un signet.

```cpp
System::SharedPtr<Aspose::Words::BookmarkEnd> Aspose::Words::DocumentBuilder::EndBookmark(const System::String &bookmarkName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | const System::String\& | Nom du signet. |

### ReturnValue

Le nœud de fin de signet qui vient d'être créé.
## Remarques


Les signets dans un document peuvent se chevaucher et couvrir n'importe quelle plage. Pour créer un signet valide, vous devez appeler à la fois [StartBookmark()](../) et [EndBookmark()](../) avec le même paramètre *bookmarkName*.

Les signets mal formés ou les signets avec des noms en double seront ignorés lors de l'enregistrement du document.

## Exemples



Montre comment créer un signet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un signet valide doit avoir le texte du corps du document entouré par
// Les nœuds BookmarkStart et BookmarkEnd créés avec un nom de signet correspondant.
builder->StartBookmark(u"MyBookmark");
builder->Writeln(u"Hello world!");
builder->EndBookmark(u"MyBookmark");

ASSERT_EQ(1, doc->get_Range()->get_Bookmarks()->get_Count());
ASSERT_EQ(u"MyBookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());
ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Text().Trim());
```


Montre comment insérer un hyperlien qui référence un signet local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartBookmark(u"Bookmark1");
builder->Write(u"Bookmarked text. ");
builder->EndBookmark(u"Bookmark1");
builder->Writeln(u"Text outside of the bookmark.");

// Insérez un champ HYPERLINK qui pointe vers le signet. Nous pouvons passer des commutateurs de champ
// à la méthode "InsertHyperlink" dans le cadre de l'argument contenant le nom du signet référencé.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
auto hyperlink = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertHyperlink(u"Link to Bookmark1", u"Bookmark1", true));
hyperlink->set_ScreenTip(u"Hyperlink Tip");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

## Voir aussi

* Class [BookmarkEnd](../../bookmarkend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
