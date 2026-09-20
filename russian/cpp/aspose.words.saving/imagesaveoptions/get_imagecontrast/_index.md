---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast метод"
linktitle: "get_ImageContrast"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast метод. Получает или задает контраст генерируемых изображений в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_imagecontrast/
---
## ImageSaveOptions::get_ImageContrast method


Получает или задаёт контраст генерируемых изображений.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast() const
```

## Примечания


Это свойство действует только при сохранении в растровые форматы изображений.

Значение по умолчанию — 0,5. Значение должно находиться в диапазоне от 0 до 1.

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

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
