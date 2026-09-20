---
title: "Метод Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias"
linktitle: "get_ImagesFolderAlias"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias. Указывает имя папки, используемой для построения URI изображений, записываемых в документ. По умолчанию пустая строка в C++."
type: docs
weight: 5500
url: /ru/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


Указывает имя папки, используемой для построения URI изображений, записываемых в документ. По умолчанию — пустая строка.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## Примечания


Когда вы сохраняете [Document](../../../aspose.words/document/) в формате [Markdown](../../../aspose.words/saveformat/), Aspose.Words необходимо сохранить все встроенные в документ изображения как отдельные файлы. [ImagesFolder](../get_imagesfolder/) позволяет указать, куда будут сохраняться изображения, а [ImagesFolderAlias](./) позволяет задать, как будут построены URI изображений.

Если [ImagesFolderAlias](./) не является пустой строкой, то URI изображения, записываемый в Markdown, будет *ImagesFolderAlias + <image file name>*.

Если [ImagesFolderAlias](./) является пустой строкой, то URI изображения, записываемый в Markdown, будет *ImagesFolder + <image file name>*.

Если [ImagesFolderAlias](./) установлен в '.' (точка), то имя файла изображения будет записано в Markdown без пути независимо от других параметров.

## Примеры



Показывает, как указать имя папки, используемой для построения URI изображений.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// Используйте свойство "ImagesFolder", чтобы назначить папку в локальной файловой системе, в которую
// Aspose.Words сохранит все связанные изображения документа.
saveOptions->set_ImagesFolder(imagesFolder);
// Используйте свойство "ImagesFolderAlias", чтобы использовать эту папку
// при построении URI изображений вместо имени папки с изображениями.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## См. также

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
