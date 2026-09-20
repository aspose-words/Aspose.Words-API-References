---
title: "Метод Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions"
linktitle: "get_MetafileRenderingOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions. Позволяет указать, как метафайлы обрабатываются в выводе рендеринга в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Позволяет указать, как метафайлы обрабатываются в результирующем выводе.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Примечания


Когда указано [Vector](../../metafilerenderingmode/), Aspose.Words сначала рендерит метафайл в векторную графику, используя собственный движок рендеринга метафайлов, а затем рендерит векторную графику в изображение.

Когда указано [Bitmap](../../metafilerenderingmode/), Aspose.Words рендерит метафайл напрямую в изображение, используя движок рендеринга метафайлов GDI+.

Движок рендеринга метафайлов GDI+ работает быстрее, поддерживает почти все возможности метафайлов, но при низких разрешениях может давать несогласованные результаты по сравнению с остальной векторной графикой (особенно с текстом) на странице. Движок рендеринга метафайлов Aspose.Words будет давать более согласованные результаты даже при низких разрешениях, но работает медленнее и может некорректно рендерить сложные метафайлы.

Значение по умолчанию для [MetafileRenderingMode](../../metafilerenderingmode/) — [Bitmap](../../metafilerenderingmode/).

## Примеры



Показывает, как установить режим рендеринга при сохранении документов с изображениями Windows Metafile в другие форматы изображений.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// Когда мы сохраняем документ как изображение, мы можем передать объект SaveOptions в
// Определяет, как операция сохранения будет обрабатывать Windows Metafile в документе.
// Если мы установим свойство "RenderingMode" в значение "MetafileRenderingMode.Vector",
// или "MetafileRenderingMode.VectorWithFallback", мы будем рендерить все метафайлы как векторную графику.
// Если мы установим свойство "RenderingMode" в значение "MetafileRenderingMode.Bitmap", мы будем рендерить все метафайлы как растровые изображения.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words использует GDI+ для эмуляции растровых операций, когда значение установлено в true.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## См. также

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
