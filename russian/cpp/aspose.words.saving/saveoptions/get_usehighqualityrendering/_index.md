---
title: "Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering метод"
linktitle: "get_UseHighQualityRendering"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering метод. Получает или задаёт значение, определяющее, использовать ли высококачественные (т.е. медленные) алгоритмы рендеринга в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.saving/saveoptions/get_usehighqualityrendering/
---
## SaveOptions::get_UseHighQualityRendering method


Получает или задаёт значение, определяющее, использовать ли высококачественные (т.е. медленные) алгоритмы рендеринга.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering() const
```

## Примечания


Значение по умолчанию — **false**.

Это свойство используется, когда документ экспортируется в форматы изображений: [Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/).

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
