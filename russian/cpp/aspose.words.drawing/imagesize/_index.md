---
title: "Aspose::Words::Drawing::ImageSize класс"
linktitle: "ImageSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ImageSize класс. Содержит информацию о размере изображения и разрешении. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.drawing/imagesize/
---
## ImageSize class


Содержит информацию о размере изображения и разрешении. Чтобы узнать больше, посетите статью документации [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/) .

```cpp
class ImageSize : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_HeightPixels](./get_heightpixels/)() const | Получает высоту изображения в пикселях. |
| [get_HeightPoints](./get_heightpoints/)() | Получает высоту изображения в пунктах. 1 пункт = 1/72 дюйма. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Получает горизонтальное разрешение в DPI. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Получает вертикальное разрешение в DPI. |
| [get_WidthPixels](./get_widthpixels/)() const | Получает ширину изображения в пикселях. |
| [get_WidthPoints](./get_widthpoints/)() | Получает ширину изображения в пунктах. 1 пункт = 1/72 дюйма. |
| [GetType](./gettype/)() const override |  |
| [ImageSize](./imagesize/)(int32_t, int32_t) | Инициализирует ширину и высоту заданными значениями в пикселях. Инициализирует разрешение до 96 dpi. |
| [ImageSize](./imagesize/)(int32_t, int32_t, double, double) | Инициализирует ширину, высоту и разрешение заданными значениями. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
