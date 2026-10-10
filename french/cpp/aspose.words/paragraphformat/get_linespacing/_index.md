---
title: "Méthode Aspose::Words::ParagraphFormat::get_LineSpacing"
linktitle: "get_LineSpacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphFormat::get_LineSpacing. Obtient ou définit l’interligne (en points) du paragraphe en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words/paragraphformat/get_linespacing/
---
## ParagraphFormat::get_LineSpacing method


Obtient ou définit l'espacement des lignes (en points) pour le paragraphe.

```cpp
double Aspose::Words::ParagraphFormat::get_LineSpacing()
```

## Remarques


Lorsque la propriété [LineSpacingRule](../get_linespacingrule/) est définie sur [AtLeast](../../linespacingrule/), l’interligne peut être supérieur ou égal, mais jamais inférieur à la valeur spécifiée de [LineSpacing](./).

Lorsque la propriété [LineSpacingRule](../get_linespacingrule/) est définie sur [Exactly](../../linespacingrule/), l’interligne ne change jamais par rapport à la valeur spécifiée de [LineSpacing](./), même si une police plus grande est utilisée dans le paragraphe.

## Exemples



Montre comment travailler avec l'espacement des lignes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Voici trois règles d'espacement des lignes que nous pouvons définir en utilisant le
// propriété "LineSpacingRule" du paragraphe pour configurer l'espacement entre les paragraphes.
// 1 -  Définir une quantité minimale d'espacement.
// Cela donnera un remplissage vertical aux lignes de texte de toute taille
// qui sont trop petites pour maintenir la hauteur de ligne minimale.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  Définir un espacement exact.
// Utiliser des tailles de police trop grandes pour l'espacement tronquera le texte.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  Définir l'espacement comme un multiple de l'espacement de ligne par défaut, qui est de 12 points par défaut.
// Ce type d'espacement s'adaptera à différentes tailles de police.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
