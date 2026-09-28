---
title: "Метод Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias"
linktitle: "get_ImagesFolderAlias"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias. Указывает имя папки, используемой для построения URI изображений, записываемых в документ XAML. По умолчанию — пустая строка в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


Указывает имя папки, используемой для построения URI изображений, записываемых в документ XAML. По умолчанию — пустая строка.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## Примечания


Когда вы сохраняете [Document](../../../aspose.words/document/) в формате XAML, Aspose.Words необходимо сохранять все изображения, встроенные в документ, как отдельные файлы. [ImagesFolder](../get_imagesfolder/) позволяет указать, где будут сохраняться изображения, а [ImagesFolderAlias](./) позволяет задать, как будут формироваться URI изображений.

Если [ImagesFolderAlias](./) не является пустой строкой, то URI изображения, записанный в XAML, будет *ImagesFolderAlias + <image file name>*.

Если [ImagesFolderAlias](./) является пустой строкой, то URI изображения, записанный в XAML, будет *ImagesFolder + <image file name>*.

Если [ImagesFolderAlias](./) установлен в '.' (точка), то имя файла изображения будет записано в XAML без пути независимо от других параметров.

## См. также

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
