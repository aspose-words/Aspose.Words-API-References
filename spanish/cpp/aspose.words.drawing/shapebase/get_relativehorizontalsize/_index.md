---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize método"
linktitle: "get_RelativeHorizontalSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize método. Obtiene o establece el valor del tamaño relativo de la forma en la dirección horizontal en C++."
type: docs
weight: 42500
url: /es/cpp/aspose.words.drawing/shapebase/get_relativehorizontalsize/
---
## ShapeBase::get_RelativeHorizontalSize method


Obtiene o establece el valor del tamaño relativo de la forma en dirección horizontal.

```cpp
Aspose::Words::Drawing::RelativeHorizontalSize Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize()
```

## Observaciones


El valor predeterminado es [RelativeHorizontalSize](../../relativehorizontalsize/).

Solo tiene efecto si [WidthRelative](../get_widthrelative/) está configurado.

## Ejemplos



Muestra cómo establecer el tamaño y la posición relativos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregar una forma simple con tamaño y posición absolutos.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// Establezca WrapType a WrapType.None ya que las formas Inline se convierten automáticamente a unidades absolutas.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Comprobando y estableciendo el tamaño horizontal relativo.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // Estableciendo la vinculación del tamaño horizontal a Margin.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // Estableciendo el ancho al 50 % del ancho de Margin.
    shape->set_WidthRelative(50.0f);
}

// Comprobando y estableciendo el tamaño vertical relativo.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // Estableciendo la vinculación del tamaño vertical a Margin.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // Estableciendo la altura al 30 % de la altura de Margin.
    shape->set_HeightRelative(30.0f);
}

// Comprobando y estableciendo la posición vertical relativa.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // Estableciendo la vinculación de posición a TopMargin.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // Estableciendo Top relativo al 30 % de la posición de TopMargin.
    shape->set_TopRelative(30.0f);
}

// Comprobando y estableciendo la posición horizontal relativa.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // Estableciendo la vinculación de posición a RightMargin.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // El valor relativo de posición puede ser negativo.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## Ver también

* Enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
