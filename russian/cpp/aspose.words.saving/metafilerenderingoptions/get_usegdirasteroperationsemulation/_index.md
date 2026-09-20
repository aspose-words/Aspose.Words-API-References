---
title: "метод Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation. Получает или задает значение, определяющее, использовать ли GDI+ для эмуляции растровых операций в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


Получает или задает значение, определяющее, следует ли использовать GDI+ для эмуляции растровых операций.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## Примечания


Библиотека Windows GDI+ может использоваться для эмуляции растровых операций. Она обеспечивает поддержку всех растровых операций по сравнению с собственной эмуляцией Aspose.Words, но в некоторых случаях производительность может быть ниже.

Когда это значение установлено в **true**, Aspose.Words использует GDI+ для эмуляции растровых операций.

Когда это значение установлено в **false**, Aspose.Words использует собственную реализацию эмуляции растровых операций.

Эта опция используется только когда метафайл рендерится как векторная графика.

Значение по умолчанию — **false**.

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

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
