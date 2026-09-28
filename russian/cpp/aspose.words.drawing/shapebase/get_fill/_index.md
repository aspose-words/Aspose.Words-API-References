---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_Fill"
linktitle: "get_Fill"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_Fill. Получает параметры заливки для фигуры в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.drawing/shapebase/get_fill/
---
## ShapeBase::get_Fill method


Получает формат заливки для фигуры.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Fill> Aspose::Words::Drawing::ShapeBase::get_Fill()
```


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

* Class [Fill](../../fill/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
