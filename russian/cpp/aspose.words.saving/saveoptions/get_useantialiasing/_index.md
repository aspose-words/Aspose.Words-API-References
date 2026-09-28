---
title: "метод Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing"
linktitle: "get_UseAntiAliasing"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing. Получает или задает значение, определяющее, использовать ли сглаживание при рендеринге в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


Получает или задаёт значение, определяющее, использовать ли сглаживание при рендеринге.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## Примечания


Значение по умолчанию — **false**. Когда это значение установлено в **true**, для рендеринга используется сглаживание.

Это свойство используется, когда документ экспортируется в следующие форматы: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/). Когда документ экспортируется в форматы [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) или [Mobi](../../../aspose.words/saveformat/), эта опция используется для растровых изображений.

## Примеры



Показывает, как улучшить качество отрисованного документа с помощью [SaveOptions](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
