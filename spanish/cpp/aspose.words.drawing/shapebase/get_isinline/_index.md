---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline método"
linktitle: "get_IsInline"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline método. Una forma rápida de determinar si esta forma está posicionada en línea con el texto en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


Una forma rápida de determinar si esta forma está posicionada en línea con el texto.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## Observaciones


Tiene efecto solo para formas de nivel superior.

## Ejemplos



Muestra cómo determinar si una forma está en línea o flotante.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos tipos de ajuste que pueden tener las formas.
// 1 -  En línea:
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// Una forma en línea se encuentra dentro de un párrafo junto a otros elementos del párrafo, como secuencias de texto.
// En Microsoft Word, podemos hacer clic y arrastrar la forma a cualquier párrafo como si fuera un carácter.
// Si la forma es grande, afectará el espaciado vertical del párrafo.
// No podemos mover esta forma a un lugar sin párrafo.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  Flotante:
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// Una forma flotante pertenece al párrafo en el que la insertamos,
// lo cual podemos determinar mediante un símbolo de anclaje que aparece al hacer clic en la forma.
// Si la forma no tiene un símbolo de anclaje visible a su izquierda,
// necesitaremos habilitar los anclajes visibles a través de "Options" -> "Display" -> "Object Anchors".
// En Microsoft Word, podemos hacer clic izquierdo y arrastrar esta forma libremente a cualquier ubicación.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## Ver también

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
