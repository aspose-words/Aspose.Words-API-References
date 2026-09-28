---
title: "Aspose::Words::Saving::ImageBinarizationMethod enum"
linktitle: "ImageBinarizationMethod"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageBinarizationMethod enum. Указывает метод, используемый для бинаризации изображения в C++."
type: docs
weight: 63000
url: /ru/cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


Указывает метод, используемый для бинаризации изображения.

```cpp
enum class ImageBinarizationMethod
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Threshold | 0 | Указывает метод порога. |
| FloydSteinbergDithering | 1 | Указывает дизеринг с использованием метода диффузии ошибки Флойда-Стейнберга. |


## Примеры



Показывает, как установить порог ошибки бинаризации TIFF при использовании метода Флойда-Стейнберга для рендеринга TIFF‑изображения.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Когда мы сохраняем документ как TIFF, мы можем передать объект SaveOptions, чтобы
// отрегулировать дизеринг, который Aspose.Words применит при рендеринге этого изображения.
// Значение свойства "ThresholdForFloydSteinbergDithering" по умолчанию равно 128.
// Более высокие значения, как правило, приводят к более тёмным изображениям.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
