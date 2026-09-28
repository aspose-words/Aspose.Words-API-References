---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize метод"
linktitle: "get_RelativeVerticalSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize метод. Получает или задает значение относительного размера фигуры по вертикальному направлению в C++."
type: docs
weight: 43500
url: /ru/cpp/aspose.words.drawing/shapebase/get_relativeverticalsize/
---
## ShapeBase::get_RelativeVerticalSize method


Получает или задает значение относительного размера фигуры в вертикальном направлении.

```cpp
Aspose::Words::Drawing::RelativeVerticalSize Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize()
```

## Примечания


Значение по умолчанию — [Margin](../../relativeverticalsize/).

Имеет эффект только если установлен [HeightRelative](../get_heightrelative/).

## Примеры



Показывает, как задать относительный размер и позицию.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавление простой фигуры с абсолютным размером и позицией.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// Установите WrapType в WrapType.None, так как встроенные фигуры автоматически преобразуются в абсолютные единицы.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Проверка и установка относительного горизонтального размера.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // Установка привязки горизонтального размера к Margin.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // Установка ширины в 50% от ширины Margin.
    shape->set_WidthRelative(50.0f);
}

// Проверка и установка относительного вертикального размера.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // Установка привязки вертикального размера к Margin.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // Установка высоты в 30% от высоты Margin.
    shape->set_HeightRelative(30.0f);
}

// Проверка и установка относительной вертикальной позиции.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // Установка привязки позиции к TopMargin.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // Установка относительного Top в 30% от позиции TopMargin.
    shape->set_TopRelative(30.0f);
}

// Проверка и установка относительной горизонтальной позиции.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // Установка привязки позиции к RightMargin.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // Относительное значение позиции может быть отрицательным.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## См. также

* Enum [RelativeVerticalSize](../../relativeverticalsize/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
