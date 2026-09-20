---
title: "метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder"
linktitle: "get_ResourcesFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder. Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат Html. По умолчанию null в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_resourcesfolder/
---
## HtmlFixedSaveOptions::get_ResourcesFolder method


Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат Html. Значение по умолчанию — **null**.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder() const
```

## Примечания


Действует только если свойство [ExportEmbeddedImages](../get_exportembeddedimages/) имеет значение **false**.

Когда вы сохраняете [Document](../../../aspose.words/document/) в формате Html, Aspose.Words необходимо сохранять все встроенные в документ изображения как отдельные файлы. [ResourcesFolder](./) позволяет указать, где будут сохраняться изображения, а [ResourcesFolderAlias](../get_resourcesfolderalias/) позволяет задать, как будут формироваться URI изображений.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранён файл документа. Используйте [ResourcesFolder](./), чтобы переопределить это поведение.

Если вы сохраняете документ в поток, у Aspose.Words нет папки для сохранения изображений, но всё равно необходимо где‑то их сохранять. В этом случае нужно указать доступную папку, используя свойство [ResourcesFolder](./).

## См. также

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
