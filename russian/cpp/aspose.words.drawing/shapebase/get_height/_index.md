---
title: "Aspose::Words::Drawing::ShapeBase::get_Height метод"
linktitle: "get_Height"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Height метод. Получает или задает высоту содержащего блока фигуры в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.drawing/shapebase/get_height/
---
## ShapeBase::get_Height method


Получает или задает высоту содержащего блока фигуры.

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Height()
```

## Примечания


Для фигуры верхнего уровня значение задаётся в пунктах.

Для фигур в группе значение находится в системе координат и единицах родительской группы.

Значение по умолчанию равно 0.

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


Показывает, как изменить размер фигуры с изображением.
```cpp
// Когда мы вставляем изображение, используя метод "InsertImage", построитель масштабирует фигуру, отображающую изображение, так что,
// когда мы просматриваем документ с масштабом 100 % в Microsoft Word, фигура отображает изображение в его реальном размере.
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Изображение 400×400 создаст объект ImageData с размером изображения 300×300 pt.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Если размеры фигуры соответствуют размерам данных изображения,
// то фигура отображает изображение в его оригинальном размере.
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// Уменьшите общий размер фигуры на 50 %.
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// Коэффициенты масштабирования применяются одновременно к ширине и высоте, чтобы сохранить пропорции фигуры.
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// Когда мы изменяем размер фигуры, размер данных изображения остаётся прежним.
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// Мы можем использовать размеры данных изображения для применения масштабирования, основанного на размере изображения.
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
