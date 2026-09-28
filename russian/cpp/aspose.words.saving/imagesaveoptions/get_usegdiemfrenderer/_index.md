---
title: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer метод"
linktitle: "get_UseGdiEmfRenderer"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer метод. Получает или задаёт значение, определяющее, использовать ли рендерер метафайлов GDI+ или Aspose.Words при сохранении в EMF в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


Получает или задает значение, определяющее, использовать ли GDI+ или рендерер метафайлов Aspose.Words при сохранении в EMF.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## Примечания


Если установлено в **true**, используется рендерер метафайлов GDI+. Т.е. содержимое записывается в графический объект GDI+ и сохраняется в метафайл.

Если установлено в **false**, используется рендерер метафайлов Aspose.Words. Т.е. содержимое записывается напрямую в формат метафайла с помощью Aspose.Words.

Имеет эффект только при сохранении в EMF.

Сохранение GDI+ работает только на .NET.

Значение по умолчанию — **true**.

## Примеры



Показывает, как выбрать рендерер при конвертации документа в .emf.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Когда мы сохраняем документ как изображение EMF, мы можем передать объект SaveOptions, чтобы выбрать рендерер для изображения.
// Если мы установим флаг "UseGdiEmfRenderer" в "true", Aspose.Words будет использовать рендерер GDI+.
// Если установить флаг "UseGdiEmfRenderer" в значение "false", Aspose.Words будет использовать собственный рендерер метафайлов.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## См. также

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
