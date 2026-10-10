---
title: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade méthode"
linktitle: "get_ForeTintAndShade"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade méthode. Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait en C++."
type: docs
weight: 10667
url: /fr/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan du trait.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## Remarques


Les valeurs autorisées se situent dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété. Zéro (0) est neutre. Tenter de définir cette propriété à une valeur inférieure à -1 ou supérieure à 1 entraîne une [ArgumentOutOfRangeException](../).

## Exemples



Montre comment définir la couleur de thème de premier plan ainsi que la teinte et l'ombrage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Voir aussi

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
