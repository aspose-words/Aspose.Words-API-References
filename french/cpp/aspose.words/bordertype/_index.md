---
title: "Aspose::Words::BorderType enum"
linktitle: "BorderType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderType enum. Spécifie les côtés d'une bordure. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 81000
url: /fr/cpp/aspose.words/bordertype/
---
## BorderType enum


Spécifie les côtés d'une bordure. Pour en savoir plus, consultez l'article de documentation [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
enum class BorderType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | -1 | Valeur par défaut. |
| Bottom | 0 | Spécifie la bordure inférieure d'un paragraphe ou d'une cellule de tableau. |
| Gauche | 1 | Spécifie la bordure gauche d'un paragraphe ou d'une cellule de tableau. |
| Droite | 2 | Spécifie la bordure droite d'un paragraphe ou d'une cellule de tableau. |
| Top | 3 | Spécifie la bordure supérieure d'un paragraphe ou d'une cellule de tableau. |
| Horizontal | 4 | Spécifie la bordure horizontale entre les cellules d'un tableau ou entre des paragraphes conformes. |
| Vertical | 5 | Spécifie la bordure verticale entre les cellules d'un tableau. |
| DiagonalDown | 6 | Spécifie la bordure diagonale dans une cellule de tableau. |
| DiagonalUp | 7 | Spécifie la bordure diagonale dans une cellule de tableau. |


## Exemples



Montre comment insérer un paragraphe avec une bordure supérieure.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Définissez ThemeColor uniquement lorsque LineWidth ou LineStyle sont définis.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
