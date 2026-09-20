---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_Left"
linktitle: "get_Left"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_Left. Получает или задаёт позицию левого края содержащего блока фигуры в C++."
type: docs
weight: 38000
url: /ru/cpp/aspose.words.drawing/shapebase/get_left/
---
## ShapeBase::get_Left method


Получает или задает позицию левого края содержащего блока фигуры.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Left()
```

## Примечания


Для формы верхнего уровня значение задаётся в пунктах и относительно привязки формы.

Для фигур в группе значение находится в системе координат и единицах родительской группы.

Значение по умолчанию равно 0.

Имеет эффект только для плавающих форм.

## Примеры



Показывает, как вставить плавающее изображение и указать его позицию и размер.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Настройте свойство формы "RelativeHorizontalPosition", чтобы рассматривать значение свойства "Left"
// как горизонтальное расстояние формы в пунктах от левой стороны страницы.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Установите горизонтальное расстояние формы от левой стороны страницы в 100.
shape->set_Left(100);

// Используйте свойство "RelativeVerticalPosition" аналогичным образом, чтобы разместить форму на 80 пунктов ниже верхней части страницы.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Установите высоту формы, при этом ширина будет автоматически масштабироваться для сохранения пропорций.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Свойства "Bottom" и "Right" содержат нижнюю и правую границы изображения.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
