---
title: "Aspose::Words::ParagraphFormat::get_LineSpacingRule méthode"
linktitle: "get_LineSpacingRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_LineSpacingRule méthode. Obtient ou définit l'interligne du paragraphe en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words/paragraphformat/get_linespacingrule/
---
## ParagraphFormat::get_LineSpacingRule method


Obtient ou définit l'espacement des lignes pour le paragraphe.

```cpp
Aspose::Words::LineSpacingRule Aspose::Words::ParagraphFormat::get_LineSpacingRule()
```


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

* Enum [LineSpacingRule](../../linespacingrule/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
