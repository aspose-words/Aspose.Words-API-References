---
title: "Метод Aspose::Words::Drawing::ImageSize::get_HeightPixels"
linktitle: "get_HeightPixels"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ImageSize::get_HeightPixels. Возвращает высоту изображения в пикселях в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing/imagesize/get_heightpixels/
---
## ImageSize::get_HeightPixels method


Получает высоту изображения в пикселях.

```cpp
int32_t Aspose::Words::Drawing::ImageSize::get_HeightPixels() const
```


## Примеры



Показывает, как прочитать свойства изображения в фигуре.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте фигуру в документ, содержащую изображение, взятое из локальной файловой системы.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Если фигура содержит изображение, её свойство ImageData будет действительным,
// и оно будет содержать объект ImageSize.
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// Объект ImageSize содержит только для чтения информацию об изображении внутри фигуры.
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// Мы можем задавать размер фигуры, исходя из размера её изображения, чтобы избежать растягивания изображения.
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## См. также

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
