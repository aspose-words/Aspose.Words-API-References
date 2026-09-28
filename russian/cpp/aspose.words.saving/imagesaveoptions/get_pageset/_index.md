---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet method"
linktitle: "get_PageSet"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageSet method. Получает или задает страницы для рендеринга. По умолчанию — все страницы документа в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_pageset/
---
## ImageSaveOptions::get_PageSet method


Получает или задает страницы для рендеринга. По умолчанию — все страницы документа.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::ImageSaveOptions::get_PageSet()
```

## Примечания


Это свойство действует только при рендеринге страниц документа. Это свойство игнорируется при рендеринге фигур в изображения.

## Примеры



Показывает, как отобразить одну страницу документа в изображение JPEG.
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
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Установите "PageSet" в "1", чтобы выбрать вторую страницу через
// ноль‑базовый индекс, с которого начинать отображение документа.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Когда мы сохраняем документ в формате JPEG, Aspose.Words отображает только одну страницу.
// Это изображение будет содержать одну страницу, начиная со второй страницы,
// которая будет просто второй страницей оригинального документа.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```


Показывает, как указать, какую страницу документа отобразить как изображение.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world! This is page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"This is page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"This is page 3.");

ASSERT_EQ(3, doc->get_PageCount());

// При сохранении документа в виде изображения Aspose.Words по умолчанию рендерит только первую страницу.
// Мы можем передать объект SaveOptions, чтобы указать другую страницу для рендеринга.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Gif);
// Отрендерить каждую страницу документа в отдельный файл изображения.
for (int32_t i = 1; i <= doc->get_PageCount(); i++)
{
    saveOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageIndex.Page {0}.gif", i), saveOptions);
}
```


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


Показывает, как извлекать страницы на основе точных диапазонов страниц.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
auto pageSet = System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<System::SharedPtr<Aspose::Words::Saving::PageRange>>({System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 3), System::MakeObject<Aspose::Words::Saving::PageRange>(2, 4), System::MakeObject<Aspose::Words::Saving::PageRange>(1, 1)}));

imageOptions->set_PageSet(pageSet);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

## См. также

* Class [PageSet](../../pageset/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
