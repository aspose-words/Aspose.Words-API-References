---
title: "Aspose::Words::Drawing::FlipOrientation enum"
linktitle: "FlipOrientation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::FlipOrientation enum. Возможные значения ориентации фигуры в C++."
type: docs
weight: 23000
url: /ru/cpp/aspose.words.drawing/fliporientation/
---
## FlipOrientation enum


Возможные значения ориентации фигуры.

```cpp
enum class FlipOrientation
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Координаты не инвертированы. |
| Горизонтальная | 1 | Отразить вдоль оси y, инвертируя координаты x. |
| Вертикальная | 2 | Отразить вдоль оси x, инвертируя координаты y. |
| Both | 3 | Отразить вдоль обеих осей y и x. |


## Примеры



Показывает, как отразить фигуру по оси.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте форму изображения и оставьте её ориентацию в состоянии по умолчанию.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

ASSERT_EQ(Aspose::Words::Drawing::FlipOrientation::None, shape->get_FlipOrientation());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Установите свойство "FlipOrientation" в "FlipOrientation.Horizontal", чтобы отразить вторую форму вдоль оси y,
// превратив её в горизонтальное зеркальное отражение первой формы.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Horizontal);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Установите свойство "FlipOrientation" в "FlipOrientation.Horizontal", чтобы отразить третью форму вдоль оси x,
// превратив её в вертикальное зеркальное отражение первой формы.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Vertical);

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 250, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 250, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");

// Установите свойство "FlipOrientation" в "FlipOrientation.Horizontal", чтобы отразить четвертую форму вдоль обеих осей x и y,
// превратив её в горизонтальное и вертикальное зеркальное отражение первой формы.
shape->set_FlipOrientation(Aspose::Words::Drawing::FlipOrientation::Both);

doc->Save(get_ArtifactsDir() + u"Shape.FlipShapeOrientation.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
