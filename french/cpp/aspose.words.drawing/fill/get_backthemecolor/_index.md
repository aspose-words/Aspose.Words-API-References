---
title: "Aspose::Words::Drawing::Fill::get_BackThemeColor méthode"
linktitle: "get_BackThemeColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Fill::get_BackThemeColor. Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing/fill/get_backthemecolor/
---
## Fill::get_BackThemeColor method


Obtient ou définit un objet ThemeColor qui représente la couleur d'arrière-plan du remplissage.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_BackThemeColor()
```


## Exemples



Montre comment définir la couleur du thème pour la couleur de forme avant-plan/arrière-plan.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Remarque : n'utilisez pas "BackThemeColor" et "BackTintAndShade" pour le remplissage de police.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## Voir aussi

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
