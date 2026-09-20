---
title: "Aspose::Words::Drawing::Fill::get_BackColor método"
linktitle: "get_BackColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Fill::get_BackColor method. Obtiene o establece un objeto Color que representa el color de fondo del relleno en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.drawing/fill/get_backcolor/
---
## Fill::get_BackColor method


Obtiene o establece un objeto Color que representa el color de fondo del relleno.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_BackColor()
```


## Ejemplos



Muestra cómo rellenar una forma con degradados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Aplicar relleno degradado de un color a la forma con ForeColor del relleno degradado.
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// Aplicar relleno degradado de dos colores a la forma.
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// Cambiar BackColor del relleno degradado.
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// Nota que cambia "GradientAngle" para "GradientStyle.FromCorner/GradientStyle.FromCenter"
// El relleno degradado no tiene ningún efecto, solo funcionará para degradados lineales.
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// Utiliza la opción de cumplimiento para definir la forma usando DML si deseas obtener "GradientStyle",
// "GradientVariant" y "GradientAngle" propiedades después de que el documento se guarde.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## Ver también

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
