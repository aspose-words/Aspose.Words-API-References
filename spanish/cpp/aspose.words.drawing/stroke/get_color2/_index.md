---
title: "Aspose::Words::Drawing::Stroke::get_Color2 método"
linktitle: "get_Color2"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Stroke::get_Color2 método. Define un segundo color para un trazo en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing/stroke/get_color2/
---
## Stroke::get_Color2 method


Define un segundo color para un trazo.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Stroke::get_Color2()
```

## Observaciones


El valor predeterminado para un [Shape](../../shape/) es **White**.

## Ejemplos



Muestra cómo procesar las características del trazo de forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// Los trazos pueden tener dos colores, que se utilizan para crear un patrón definido por datos de imagen en dos tonos.
// Los trazos con un solo color no utilizan la propiedad Color2.
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## Ver también

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
