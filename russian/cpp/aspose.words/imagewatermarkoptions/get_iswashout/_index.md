---
title: "Метод Aspose::Words::ImageWatermarkOptions::get_IsWashout"
linktitle: "get_IsWashout"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ImageWatermarkOptions::get_IsWashout. Получает или задает логическое значение, отвечающее за эффект выцветания водяного знака. Значение по умолчанию — true в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Получает или задает логическое значение, отвечающее за эффект вымывания водяного знака. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


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
