---
title: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor método"
linktitle: "get_ForeThemeColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor método. Obtiene o establece un objeto ThemeColor que representa el color de primer plano del trazo en C++."
type: docs
weight: 10334
url: /es/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


Obtiene o establece un objeto ThemeColor que representa el color de primer plano del trazo.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


## Ejemplos



Muestra cómo establecer el color de tema de primer plano y el tinte y la sombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## Ver también

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
