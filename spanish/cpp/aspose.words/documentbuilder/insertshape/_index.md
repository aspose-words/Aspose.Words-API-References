---
title: "Aspose::Words::DocumentBuilder::InsertShape method"
linktitle: "InsertShape"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertShape method. Inserta una forma flotante con posición, tamaño y tipo de ajuste de texto especificados en C++."
type: docs
weight: 45000
url: /es/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserta una forma flotante libre con la posición, tamaño y tipo de ajuste de texto especificados.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | El tipo de forma a insertar en el documento |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia horizontal a la forma. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la forma. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia vertical a la forma. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la forma. |
| ancho | double | El ancho de la forma en puntos. |
| alto | double | La altura de la forma en puntos. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la forma. |

### ReturnValue

El nodo de forma que se insertó.

## Ejemplos



Muestra cómo insertar formas DML en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos tipos de ajuste que pueden tener las formas.
// 1 -  Flotante:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  En línea:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Si necesita crear formas "no primitivas", como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
// entonces guarde el documento con cumplimiento "Strict" o "Transitional", lo que permite guardar la forma como DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


Inserta una forma en línea con el tipo y tamaño especificados.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | El tipo de forma a insertar en el documento. |
| ancho | double | El ancho de la forma en puntos. |
| alto | double | La altura de la forma en puntos. |

### ReturnValue

El nodo de forma que se insertó.

## Ejemplos



Muestra cómo insertar formas DML en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos tipos de ajuste que pueden tener las formas.
// 1 -  Flotante:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  En línea:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Si necesita crear formas "no primitivas", como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
// entonces guarde el documento con cumplimiento "Strict" o "Transitional", lo que permite guardar la forma como DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
