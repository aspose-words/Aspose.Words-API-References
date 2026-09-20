---
title: "Aspose::Words::Drawing::Shape::get_FillColor метод"
linktitle: "get_FillColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Shape::get_FillColor метод. Определяет цвет кисти, заполняющей замкнутый контур фигуры в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.drawing/shape/get_fillcolor/
---
## Shape::get_FillColor method


Определяет цвет кисти, заполняющий замкнутый контур фигуры.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Shape::get_FillColor()
```

## Примечания


Это сокращение к свойству [Color](../../fill/get_color/).

Значение по умолчанию **White**.

## Примеры



Показывает, как залить форму сплошным цветом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Напишите некоторый текст, а затем накройте его плавающей формой.
builder->get_Font()->set_Size(32);
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::CloudCallout, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 25, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 25, 250, 150, Aspose::Words::Drawing::WrapType::None);

// Используйте свойство "StrokeColor" для установки цвета контура формы.
shape->set_StrokeColor(System::Drawing::Color::get_CadetBlue());

// Используйте свойство "FillColor" для установки цвета внутренней области формы.
shape->set_FillColor(System::Drawing::Color::get_LightBlue());

// Свойство "Opacity" определяет, насколько прозрачным является цвет по шкале от 0 до 1,
// где 1 означает полностью непрозрачный, а 0 — невидимый.
// Заполнение фигуры по умолчанию полностью непрозрачно, поэтому мы не видим текст, который находится под этой фигурой.
ASPOSE_ASSERT_EQ(1.0, shape->get_Fill()->get_Opacity());

// Установите более низкую непрозрачность цвета заполнения фигуры, чтобы мы могли видеть текст под ней.
shape->get_Fill()->set_Opacity(0.3);

doc->Save(get_ArtifactsDir() + u"Shape.Fill.docx");
```

## См. также

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
