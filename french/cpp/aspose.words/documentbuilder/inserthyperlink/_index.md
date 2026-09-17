---
title: "Méthode Aspose::Words::DocumentBuilder::InsertHyperlink"
linktitle: "InsertHyperlink"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertHyperlink. Insère un hyperlien dans le document en C++."
type: docs
weight: 38000
url: /fr/cpp/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder::InsertHyperlink method


Insère un hyperlien dans le document.

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertHyperlink(const System::String &displayText, const System::String &urlOrBookmark, bool isBookmark)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| displayText | const System::String\& | Texte du lien à afficher dans le document. |
| urlOrBookmark | const System::String\& | Destination du lien. Peut être une URL ou le nom d'un signet dans le document. Cette méthode ajoute toujours des apostrophes au début et à la fin de l'URL. |
| isBookmark | bool | **true** si le paramètre précédent est le nom d'un signet dans le document ; **false** si le paramètre précédent est une URL. |

### ReturnValue

Un objet [Field](../../../aspose.words.fields/field/) qui représente le champ inséré.
## Remarques


Notez que vous devez spécifier le format de police pour le texte du lien hypertexte explicitement en utilisant la propriété [Font](../get_font/).

Cette méthode appelle en interne [InsertField()](../) pour insérer un champ HYPERLINK de MS Word dans le document.

## Exemples



Montre comment insérer un champ de lien hypertexte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Insérez un lien hypertexte et mettez‑le en évidence avec un formatage personnalisé.
// Le lien hypertexte sera un morceau de texte cliquable qui nous mènera à l'emplacement spécifié dans l'URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic gauche sur le lien dans le texte dans Microsoft Word nous amènera à l'URL via une nouvelle fenêtre de navigateur web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Montre comment utiliser la pile de formatage d'un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configure le formatage de la police, puis écris le texte qui précède le lien hypertexte.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Préserve notre configuration de formatage actuelle sur la pile.
builder->PushFont();

// Modifie le formatage actuel du builder en appliquant un nouveau style.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Restaure le formatage de la police que nous avons enregistré précédemment et supprime l'élément de la pile.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
