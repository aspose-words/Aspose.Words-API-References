---
title: "Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat метод"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat метод. Указывает формат, в котором будут сохраняться отрисованные страницы документа или фигуры, если используется этот объект параметров сохранения. Может быть растровым Tiff, Png, Bmp, Jpeg или векторным Emf, Eps, WebP, Svg в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_saveformat/
---
## ImageSaveOptions::get_SaveFormat method


Указывает формат, в котором будут сохраняться отрисованные страницы документа или фигуры, если используется этот объект параметров сохранения. Может быть растровым [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/) или векторным [Emf](../../../aspose.words/saveformat/), [Eps](../../../aspose.words/saveformat/), [WebP](../), [Svg](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat() override
```

## Примечания


Количество других параметров зависит от выбранного формата.

Также возможно сохранять в SVG как через [ImageSaveOptions](../), так и через [SvgSaveOptions](../../svgsaveoptions/).

## Примеры



Показывает, как редактировать изображение, пока Aspose.Words конвертирует документ в него.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions в
// отредактировать изображение, пока операция сохранения рендерит его.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Мы можем изменить эти свойства, чтобы изменить яркость и контраст изображения.
// Оба находятся в диапазоне от 0 до 1 и по умолчанию равны 0,5.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Мы можем настроить горизонтальное и вертикальное разрешение с помощью этих свойств.
// Это повлияет на размеры изображения.
// Значение по умолчанию для этих свойств равно 96,0 при разрешении 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Мы можем масштабировать изображение, используя это свойство. Значение по умолчанию — 1,0, что соответствует масштабированию 100 %.
// Мы можем использовать это свойство, чтобы отменить любые изменения размеров изображения, которые вызвало бы изменение разрешения.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```

## См. также

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
