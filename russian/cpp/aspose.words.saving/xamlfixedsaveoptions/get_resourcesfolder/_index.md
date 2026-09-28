---
title: "Метод Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder"
linktitle: "get_ResourcesFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder. Указывает физическую папку, в которой сохраняются ресурсы (изображения и шрифты) при экспорте документа в фиксированный Xaml-формат. По умолчанию null в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/xamlfixedsaveoptions/get_resourcesfolder/
---
## XamlFixedSaveOptions::get_ResourcesFolder method


Указывает физическую папку, в которой сохраняются ресурсы (изображения и шрифты) при экспорте документа в фиксированный Xaml‑формат. По умолчанию **null**.

```cpp
System::String Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder() const
```

## Примечания


Когда вы сохраняете [Document](../../../aspose.words/document/) в фиксированном Xaml-формате, Aspose.Words необходимо сохранять все встроенные в документ изображения как отдельные файлы. [ResourcesFolder](./) позволяет указать, где будут сохраняться изображения, а [ResourcesFolderAlias](../get_resourcesfolderalias/) позволяет задать, как будут формироваться URI изображений.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранён файл документа. Используйте [ResourcesFolder](./), чтобы переопределить это поведение.

Если вы сохраняете документ в поток, у Aspose.Words нет папки для сохранения изображений, но всё равно необходимо где‑то их сохранять. В этом случае нужно указать доступную папку, используя свойство [ResourcesFolder](./).

## См. также

* Class [XamlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
