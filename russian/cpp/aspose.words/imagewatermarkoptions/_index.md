---
title: "Класс Aspose::Words::ImageWatermarkOptions"
linktitle: "ImageWatermarkOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::ImageWatermarkOptions. Содержит параметры, которые можно указать при добавлении водяного знака с изображением. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 34000
url: /ru/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


Содержит параметры, которые можно указать при добавлении водяного знака с изображением. Чтобы узнать больше, посетите статью документации [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class ImageWatermarkOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | Получает или задает логическое значение, отвечающее за эффект вымывания водяного знака. Значение по умолчанию — **true**. |
| [get_Scale](./get_scale/)() const | Получает или задает коэффициент масштабирования, выраженный в виде доли изображения. Значение по умолчанию — 0 — авто. |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | Сеттер для [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/). |
| [set_Scale](./set_scale/)(double) | Сеттер для [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
