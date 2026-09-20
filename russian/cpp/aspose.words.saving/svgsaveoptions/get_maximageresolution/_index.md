---
title: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution метод"
linktitle: "get_MaxImageResolution"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution метод. Получает или задает значение в пикселях на дюйм, ограничивающее разрешение экспортируемых растровых изображений. Значение по умолчанию — ноль в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words.saving/svgsaveoptions/get_maximageresolution/
---
## SvgSaveOptions::get_MaxImageResolution method


Получает или задает значение в пикселях на дюйм, ограничивающее разрешение экспортируемых растровых изображений. Значение по умолчанию — ноль.

```cpp
int32_t Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution() const
```

## Примечания


Если значение этого свойства не равно нулю, оно ограничивает разрешение экспортируемых растровых изображений. То есть изображения с более высоким разрешением пересчитываются до указанного предела, а изображения с более низким разрешением экспортируются без изменений.

Если значение этого свойства равно нулю, все растровые изображения экспортируются без пересчёта.

## Примеры



Показывает, как установить ограничение разрешения изображения.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_MaxImageResolution(72);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

## См. также

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
