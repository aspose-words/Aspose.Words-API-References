---
title: "Метод Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder"
linktitle: "get_ResourcesFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder. Указывает физическую папку, куда сохраняются ресурсы (изображения) при экспорте документа в формат Svg. По умолчанию значение null в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.saving/svgsaveoptions/get_resourcesfolder/
---
## SvgSaveOptions::get_ResourcesFolder method


Указывает физическую папку, в которой сохраняются ресурсы (изображения) при экспорте документа в формат SVG. По умолчанию **null**.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder() const
```

## Примечания


Действует только если свойство [ExportEmbeddedImages](../get_exportembeddedimages/) имеет значение **false**.

Когда вы сохраняете [Document](../../../aspose.words/document/) в формате SVG, Aspose.Words необходимо сохранять все встроенные в документ изображения как отдельные файлы. [ResourcesFolder](./) позволяет указать, где будут сохраняться изображения, а [ResourcesFolderAlias](../get_resourcesfolderalias/) позволяет задать, как будут формироваться URI изображений.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранён файл документа. Используйте [ResourcesFolder](./), чтобы переопределить это поведение.

Если вы сохраняете документ в поток, у Aspose.Words нет папки для сохранения изображений, но всё равно необходимо где‑то их сохранять. В этом случае нужно указать доступную папку в свойстве [ResourcesFolder](./).

## См. также

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
