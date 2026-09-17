---
title: "Méthode Aspose::Words::Drawing::Stroke::get_ForeThemeColor"
linktitle: "get_ForeThemeColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::Stroke::get_ForeThemeColor. Obtient ou définit un objet ThemeColor qui représente la couleur de premier plan du trait en C++."
type: docs
weight: 10334
url: /fr/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


Obtient ou définit un objet ThemeColor qui représente la couleur de premier plan du trait.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
