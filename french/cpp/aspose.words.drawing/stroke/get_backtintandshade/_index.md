---
title: "Méthode Aspose::Words::Drawing::Stroke::get_BackTintAndShade"
linktitle: "get_BackTintAndShade"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Stroke::get_BackTintAndShade. Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du tracé en C++."
type: docs
weight: 2334
url: /fr/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur d'arrière-plan du trait.

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## Remarques


Les valeurs autorisées se situent dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété à une valeur inférieure à -1 ou supérieure à 1 entraîne une [ArgumentOutOfRangeException](../).

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

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
