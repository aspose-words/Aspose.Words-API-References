---
title: "Aspose::Words::ParagraphFormat::get_OutlineLevel méthode"
linktitle: "get_OutlineLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_OutlineLevel méthode. Spécifie le niveau de plan du paragraphe dans le document en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words/paragraphformat/get_outlinelevel/
---
## ParagraphFormat::get_OutlineLevel method


Spécifie le niveau de plan du paragraphe dans le document.

```cpp
Aspose::Words::OutlineLevel Aspose::Words::ParagraphFormat::get_OutlineLevel()
```


## Exemples



Montre comment configurer les niveaux de plan de paragraphe pour créer du texte pliable.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Chaque paragraphe possède un OutlineLevel, qui peut être n'importe quel nombre de 1 à 9, ou la valeur par défaut "BodyText".
// Définir la propriété sur l'une des valeurs numérotées affichera une flèche à gauche
// du début du paragraphe.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level1);
builder->Writeln(u"Paragraph outline level 1.");

// Le niveau 1 est le niveau le plus élevé. S'il y a un paragraphe de niveau inférieur sous un paragraphe de niveau supérieur,
// réduire le paragraphe de niveau supérieur masquera le paragraphe de niveau inférieur.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level2);
builder->Writeln(u"Paragraph outline level 2.");

// Deux paragraphes du même niveau ne se masqueront pas l'un l'autre,
// et les flèches ne réduisent pas les paragraphes vers lesquels elles pointent.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::Level3);
builder->Writeln(u"Paragraph outline level 3.");
builder->Writeln(u"Paragraph outline level 3.");

// La valeur par défaut "BodyText" est la plus basse, ce qu'un paragraphe de n'importe quel niveau peut réduire.
builder->get_ParagraphFormat()->set_OutlineLevel(Aspose::Words::OutlineLevel::BodyText);
builder->Writeln(u"Paragraph at main text level.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphOutlineLevel.docx");
```

## Voir aussi

* Enum [OutlineLevel](../../outlinelevel/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
