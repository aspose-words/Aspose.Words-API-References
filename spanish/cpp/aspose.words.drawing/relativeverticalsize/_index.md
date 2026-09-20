---
title: "Aspose::Words::Drawing::RelativeVerticalSize enum"
linktitle: "RelativeVerticalSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::RelativeVerticalSize enum. Especifica respecto a qué se calcula verticalmente la altura de una forma o un marco de texto en C++."
type: docs
weight: 34500
url: /es/cpp/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enum


Especifica, de forma relativa, respecto a qué se calcula verticalmente la altura de una forma o de un marco de texto.

```cpp
enum class RelativeVerticalSize
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Margen | 0 | Especifica que la altura se calcula en relación al espacio entre los márgenes superior e inferior. |
| Page | 1 | Especifica que la altura se calcula en relación a la altura de la página. |
| TopMargin | 2 | Especifica que la altura se calcula en relación al tamaño del área del margen superior. |
| BottomMargin | 3 | Especifica que la altura se calcula en relación al tamaño del área del margen inferior. |
| InnerMargin | 4 | Especifica que la altura se calcula en relación al tamaño del área del margen interior, al tamaño del área del margen superior para páginas impares y al tamaño del área del margen inferior para páginas pares. |
| OuterMargin | 5 | Especifica que la altura se calcula en relación al tamaño del área del margen exterior, al tamaño del área del margen inferior para páginas impares y al tamaño del área del margen superior para páginas pares. |
| Default | n/a | El valor predeterminado es [Margin](./). |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
