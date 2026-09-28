---
title: "Метод Aspose::Words::Saving::ImageSaveOptions::get_ImageSize"
linktitle: "get_ImageSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::ImageSaveOptions::get_ImageSize. Получает или задает размер сгенерированного изображения в пикселях в C++."
type: docs
weight: 7500
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


Получает или задаёт размер генерируемого изображения в пикселях.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## Примечания


Это свойство действует только при сохранении в растровые форматы изображений.

Значение по умолчанию — (0 x 0), что означает, что размер сгенерированного изображения будет вычисляться исходя из размера изображения в пунктах, указанного разрешения и масштаба.

## Примеры



Показывает, как отобразить каждую страницу документа в отдельное изображение TIFF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ, которым этот метод отображает документ в изображение.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Установите свойство "PageSet" в номер первой страницы от
    // с которой начинать рендеринг документа.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Экспортировать страницу с разрешением 2325x5325 пикселей и 600 dpi.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## См. также

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
