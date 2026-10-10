---
title: "Aspose::Words::Border::get_TintAndShade méthode"
linktitle: "get_TintAndShade"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Border::get_TintAndShade méthode. Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/border/get_tintandshade/
---
## Border::get_TintAndShade method


Obtient ou définit une valeur double qui éclaircit ou assombrit une couleur.

```cpp
double Aspose::Words::Border::get_TintAndShade()
```

## Remarques


Les valeurs autorisées sont dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété. Zéro (0) est neutre.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
