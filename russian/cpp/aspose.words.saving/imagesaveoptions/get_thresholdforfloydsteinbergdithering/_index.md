---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method"
linktitle: "get_ThresholdForFloydSteinbergDithering"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method. Получает или задает порог, определяющий значение ошибки бинаризации в методе Флойда‑Штайнберга, когда ImageBinarizationMethod установлен в FloydSteinbergDithering в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method


Получает или задает порог, определяющий значение ошибки бинаризации в методе Флойда‑Штайнберга, когда [ImageBinarizationMethod](../../imagebinarizationmethod/) установлен в [FloydSteinbergDithering](../../imagebinarizationmethod/).

```cpp
uint8_t Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering() const
```

## Примечания


Значение по умолчанию — 128.

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

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
