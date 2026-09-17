---
title: "Aspose::Words::DocumentBuilder::InsertParagraph méthode"
linktitle: "InsertParagraph"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertParagraph méthode. Insère un saut de paragraphe dans le document en C++."
type: docs
weight: 44000
url: /fr/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


Insère un saut de paragraphe dans le document.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

Le nœud de paragraphe qui vient d'être inséré. C'est le même nœud que [CurrentParagraph](../get_currentparagraph/).
## Remarques


Le formatage du paragraphe actuel spécifié par la propriété [ParagraphFormat](../get_paragraphformat/) est utilisé.

Divise le paragraphe actuel en deux. Après l'insertion du paragraphe, le curseur est placé au début du nouveau paragraphe.

Une exception est levée s'il n'est pas possible d'insérer un saut de paragraphe à la position actuelle du curseur.

## Exemples



Montre comment insérer un paragraphe dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// La méthode "Writeln" termine le paragraphe après avoir ajouté du texte
// et commence ensuite une nouvelle ligne, ajoutant un nouveau paragraphe.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Voir aussi

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
