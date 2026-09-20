---
title: "Método Aspose::Words::Drawing::Stroke::get_BackTintAndShade"
linktitle: "get_BackTintAndShade"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Stroke::get_BackTintAndShade. Obtiene o establece un valor double que aclara u oscurece el color de fondo del trazo en C++."
type: docs
weight: 2334
url: /es/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


Obtiene o establece un valor doble que aclara o oscurece el color de fondo del trazo.

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## Observaciones


Los valores permitidos están dentro del rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad. Cero (0) es neutral. Intentar establecer esta propiedad a un valor menor que -1 o mayor que 1 produce un [ArgumentOutOfRangeException](../).

## Ejemplos



Muestra cómo establecer el color de tema de fondo y tono y sombra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## Ver también

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
