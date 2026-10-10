---
title: "Aspose::Words::Drawing::Fill::get_BackTintAndShade método"
linktitle: "get_BackTintAndShade"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Fill::get_BackTintAndShade método. Obtiene o establece un valor doble que aclara o oscurece el color de fondo en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing/fill/get_backtintandshade/
---
## Fill::get_BackTintAndShade method


Obtiene o establece un valor double que aclara o oscurece el color de fondo.

```cpp
double Aspose::Words::Drawing::Fill::get_BackTintAndShade()
```

## Observaciones


Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad.

Cero (0) es neutral.

## Ejemplos



Muestra cómo establecer el color temático para el color de forma de primer plano/fondo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// Nota: no use "BackThemeColor" y "BackTintAndShade" para el relleno de fuente.
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## Ver también

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
