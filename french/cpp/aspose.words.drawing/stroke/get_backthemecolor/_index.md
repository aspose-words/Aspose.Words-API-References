---
title: "Aspose::Words::Drawing::Stroke::get_BackThemeColor méthode"
linktitle: "get_BackThemeColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Stroke::get_BackThemeColor méthode. Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du trait en C++."
type: docs
weight: 2167
url: /fr/cpp/aspose.words.drawing/stroke/get_backthemecolor/
---
## Stroke::get_BackThemeColor method


Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du trait.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_BackThemeColor()
```


## Exemples



Montre comment définir la couleur de thème arrière et la teinte et l'ombrage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## Voir aussi

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
