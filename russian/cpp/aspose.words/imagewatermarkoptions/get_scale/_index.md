---
title: "Aspose::Words::ImageWatermarkOptions::get_Scale метод"
linktitle: "get_Scale"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ImageWatermarkOptions::get_Scale метод. Получает или задает коэффициент масштабирования, выраженный в виде доли от изображения. Значение по умолчанию — 0 — авто в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


Получает или задает коэффициент масштабирования, выраженный в виде доли изображения. Значение по умолчанию — 0 — авто.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## Примечания


Допустимые значения находятся в диапазоне от 0 до 65,5 включительно.

Автомасштаб означает, что водяной знак будет масштабироваться до максимальной ширины и высоты относительно полей страницы.

## Примеры



Показывает, как создать водяной знак из изображения в локальной файловой системе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Измените внешний вид изображенного водяного знака с помощью объекта ImageWatermarkOptions,
// затем передайте его при создании водяного знака из файла изображения.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// У нас есть различные варианты вставки изображения.
// Используйте один из следующих методов для добавления изображенного водяного знака.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## См. также

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
