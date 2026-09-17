---
title: "Aspose::Words::Drawing::Fill::get_BackTintAndShade méthode"
linktitle: "get_BackTintAndShade"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Fill::get_BackTintAndShade méthode. Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.drawing/fill/get_backtintandshade/
---
## Fill::get_BackTintAndShade method


Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan.

```cpp
double Aspose::Words::Drawing::Fill::get_BackTintAndShade()
```

## Remarques


Les valeurs autorisées sont dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété.

Zéro (0) est neutre.

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

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
