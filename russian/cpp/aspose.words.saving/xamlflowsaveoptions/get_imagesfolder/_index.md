---
title: "Метод Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder"
linktitle: "get_ImagesFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder. Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат XAML. По умолчанию — пустая строка в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат XAML. По умолчанию — пустая строка.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## Примечания


Когда вы сохраняете [Document](../../../aspose.words/document/) в формате XAML, Aspose.Words необходимо сохранять все изображения, встроенные в документ, как отдельные файлы. [ImagesFolder](./) позволяет указать, где будут сохраняться изображения, а [ImagesFolderAlias](../get_imagesfolderalias/) позволяет задать, как будут формироваться URI изображений.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранён файл документа. Используйте [ImagesFolder](./), чтобы переопределить это поведение.

Если вы сохраняете документ в поток, у Aspose.Words нет папки для сохранения изображений, но всё равно необходимо где‑то их сохранять. В этом случае следует указать доступную папку в свойстве [ImagesFolder](./) или предоставить пользовательские потоки через обработчик события [ImageSavingCallback](../get_imagesavingcallback/).

## См. также

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
