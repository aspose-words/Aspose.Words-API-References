---
title: "Aspose::Words::Drawing::RelativeHorizontalSize enum"
linktitle: "RelativeHorizontalSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::RelativeHorizontalSize enum. Указывает относительно чего ширина формы или текстовой рамки вычисляется по горизонтали в C++."
type: docs
weight: 33500
url: /ru/cpp/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enum


Указывает, относительно чего рассчитывается ширина фигуры или текстового фрейма по горизонтали.

```cpp
enum class RelativeHorizontalSize
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Поле | 0 | Указывает, что ширина вычисляется относительно пространства между левым и правым полями. |
| Page | 1 | Указывает, что ширина вычисляется относительно ширины страницы. |
| LeftMargin | 2 | Указывает, что ширина вычисляется относительно размера области левого поля. |
| RightMargin | 3 | Указывает, что ширина вычисляется относительно размера области правого поля. |
| InnerMargin | 4 | Указывает, что ширина вычисляется относительно размера внутреннего поля, размера левого поля для нечётных страниц и размера правого поля для чётных страниц. |
| OuterMargin | 5 | Указывает, что ширина вычисляется относительно размера внешнего поля, размера правого поля для нечётных страниц и размера левого поля для чётных страниц. |
| Default | n/a | Значение по умолчанию — [Margin](./). |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
