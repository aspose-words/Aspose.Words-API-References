---
title: "Méthode Aspose::Words::Border::get_ThemeColor"
linktitle: "get_ThemeColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Border::get_ThemeColor. Obtient ou définit la couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet Border en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/border/get_themecolor/
---
## Border::get_ThemeColor method


Obtient ou définit la couleur du thème dans le schéma de couleurs appliqué qui est associé à cet objet [Border](../).

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Border::get_ThemeColor()
```


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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
