---
title: "Méthode Aspose::Words::Paragraph::get_BreakIsStyleSeparator"
linktitle: "get_BreakIsStyleSeparator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Paragraph::get_BreakIsStyleSeparator. True si ce saut de paragraphe est un séparateur de style. Un séparateur de style permet à un paragraphe de se composer de parties ayant des styles de paragraphe différents en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


True si ce saut de paragraphe est un séparateur [Style](../../style/). Un séparateur de style permet à un paragraphe de se composer de parties ayant des styles de paragraphe différents.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## Exemples



Montre comment écrire du texte sur la même ligne qu’un titre de TOC sans qu’il apparaisse dans la TOC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Insérez un paragraphe avec un style que la TOC prendra comme entrée.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// Ces deux chaînes sont dans le même paragraphe et apparaîtront donc dans la même entrée de la TOC.
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// Si nous insérons un séparateur de style, nous pouvons écrire plus de texte dans le même paragraphe
// et utiliser un style différent sans qu’il apparaisse dans la TOC.
// Si nous utilisons un style de type titre après le séparateur, nous pouvons générer plusieurs entrées de TOC à partir d’une même ligne de texte du document.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## Voir aussi

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
