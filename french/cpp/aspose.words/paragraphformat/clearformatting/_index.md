---
title: "Aspose::Words::ParagraphFormat::ClearFormatting méthode"
linktitle: "ClearFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::ClearFormatting méthode. Réinitialise le format de paragraphe par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/paragraphformat/clearformatting/
---
## ParagraphFormat::ClearFormatting method


Réinitialise le formatage du paragraphe aux valeurs par défaut.

```cpp
void Aspose::Words::ParagraphFormat::ClearFormatting()
```


## Exemples



Montre comment imbriquer une liste dans une autre liste.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Une liste nous permet d'organiser et de décorer des ensembles de paragraphes avec des symboles de préfixe et des retraits.
// Nous pouvons créer des listes imbriquées en augmentant le niveau de retrait.
// Nous pouvons commencer et terminer une liste en utilisant la propriété "ListFormat" d'un constructeur de document.
// Chaque paragraphe que nous ajoutons entre le début et la fin d'une liste deviendra un élément de la liste.
// Créez une liste de plan pour les titres.
System::SharedPtr<Aspose::Words::Lists::List> outlineList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::OutlineNumbers);
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 1");

// Créez une liste numérotée.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(numberedList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Numbered list item 1.");

// Chaque paragraphe qui comprend une liste aura ce drapeau.
ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsListItem());
ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsListItem());

// Créez une liste à puces.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
builder->get_ListFormat()->set_List(bulletedList);
builder->get_ParagraphFormat()->set_LeftIndent(72);
builder->Writeln(u"Bulleted list item 1.");
builder->Writeln(u"Bulleted list item 2.");
builder->get_ParagraphFormat()->ClearFormatting();

// Revenez à la liste numérotée.
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Numbered list item 2.");
builder->Writeln(u"Numbered list item 3.");

// Revenez à la liste de plan.
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 2");

builder->get_ParagraphFormat()->ClearFormatting();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.NestedLists.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
