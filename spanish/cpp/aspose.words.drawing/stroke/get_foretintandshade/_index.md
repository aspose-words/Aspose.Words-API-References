---
title: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade método"
linktitle: "get_ForeTintAndShade"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade método. Obtiene o establece un valor doble que aclara u oscurece el color de primer plano del trazo en C++."
type: docs
weight: 10667
url: /es/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


Obtiene o establece un valor double que aclara u oscurece el color de primer plano del trazo.

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## Observaciones


Los valores permitidos están dentro del rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad. Cero (0) es neutral. Intentar establecer esta propiedad a un valor menor que -1 o mayor que 1 produce un [ArgumentOutOfRangeException](../).

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

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
