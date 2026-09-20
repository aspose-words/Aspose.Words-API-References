---
title: "Метод Aspose::Words::DocumentBuilder::InsertShape"
linktitle: "InsertShape"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::InsertShape. Вставляет плавающую форму с указанными позицией, размером и типом обтекания текста в C++."
type: docs
weight: 45000
url: /ru/cpp/aspose.words/documentbuilder/insertshape/
---
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Вставляет плавающую форму с указанным положением, размером и типом обтекания текста.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Тип формы для вставки в документ |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Указывает, откуда измеряется горизонтальное расстояние до формы. |
| left | double | Расстояние в пунктах от начала координат до левой стороны формы. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Указывает, откуда измеряется вертикальное расстояние до фигуры. |
| top | double | Расстояние в пунктах от начала координат до верхней стороны фигуры. |
| width | double | Ширина фигуры в пунктах. |
| height | double | Высота фигуры в пунктах. |
| wrapType | Aspose::Words::Drawing::WrapType | Указывает, как обтекать текст вокруг фигуры. |

### ReturnValue

Узел фигуры, который был вставлен.

## Примеры



Показывает, как вставлять формы DML в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два типа обтекания, которые могут иметь формы.
// 1 -  Плавающая:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Встроенная:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Если вам нужно создать "непримитивные" формы, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// затем сохраните документ с соответствием "Strict" или "Transitional", что позволяет сохранять форму как DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType, double, double) method


Вставляет встроенную форму с указанным типом и размером.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertShape(Aspose::Words::Drawing::ShapeType shapeType, double width, double height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | Aspose::Words::Drawing::ShapeType | Тип фигуры для вставки в документ. |
| width | double | Ширина фигуры в пунктах. |
| height | double | Высота фигуры в пунктах. |

### ReturnValue

Узел фигуры, который был вставлен.

## Примеры



Показывает, как вставлять формы DML в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два типа обтекания, которые могут иметь формы.
// 1 -  Плавающая:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::TopCornersRounded, Aspose::Words::Drawing::RelativeHorizontalPosition::Page, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Page, 100, 50, 50, Aspose::Words::Drawing::WrapType::None);

// 2 -  Встроенная:
builder->InsertShape(Aspose::Words::Drawing::ShapeType::DiagonalCornersRounded, 50, 50);

// Если вам нужно создать "непримитивные" формы, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// затем сохраните документ с соответствием "Strict" или "Transitional", что позволяет сохранять форму как DML.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Transitional);

doc->Save(get_ArtifactsDir() + u"Shape.ShapeInsertion.docx", saveOptions);
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ShapeType](../../../aspose.words.drawing/shapetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
