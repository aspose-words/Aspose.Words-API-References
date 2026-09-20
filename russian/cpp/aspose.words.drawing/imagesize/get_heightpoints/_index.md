---
title: "Метод Aspose::Words::Drawing::ImageSize::get_HeightPoints"
linktitle: "get_HeightPoints"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ImageSize::get_HeightPoints. Возвращает высоту изображения в пунктах. 1 пункт = 1/72 дюйма в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.drawing/imagesize/get_heightpoints/
---
## ImageSize::get_HeightPoints method


Получает высоту изображения в пунктах. 1 пункт = 1/72 дюйма.

```cpp
double Aspose::Words::Drawing::ImageSize::get_HeightPoints()
```


## Примеры



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

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
