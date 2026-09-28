---
title: "Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod метод"
linktitle: "get_TiffBinarizationMethod"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod. Получает или задает метод, используемый при конвертации изображений в формат 1 bpp, когда SaveFormat равен Tiff и TiffCompression равен Ccitt3 или Ccitt4 в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_tiffbinarizationmethod/
---
## ImageSaveOptions::get_TiffBinarizationMethod method


Получает или задает метод, используемый при конвертации изображений в формат 1 bpp, когда [SaveFormat](../get_saveformat/) равен [Tiff](../../../aspose.words/saveformat/) и [TiffCompression](../get_tiffcompression/) равен [Ccitt3](../../tiffcompression/) или [Ccitt4](../../tiffcompression/).

```cpp
Aspose::Words::Saving::ImageBinarizationMethod Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod() const
```

## Примечания


Значение по умолчанию — [Threshold](../../imagebinarizationmethod/).

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

* Enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
