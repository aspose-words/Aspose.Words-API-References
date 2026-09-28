---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder метод"
linktitle: "get_ImagesFolder"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder метод. Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат Markdown. По умолчанию это пустая строка в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат [Markdown](../../../aspose.words/saveformat/). По умолчанию это пустая строка.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## Примечания


При сохранении [Document](../../../aspose.words/document/) в формате [Markdown](../../../aspose.words/saveformat/) Aspose.Words необходимо сохранять все встроенные в документ изображения как отдельные файлы. [ImagesFolder](./) позволяет указать, где будут сохраняться изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранён файл документа. Используйте [ImagesFolder](./), чтобы переопределить это поведение.

Если вы сохраняете документ в поток, у Aspose.Words нет папки для сохранения изображений, но всё равно необходимо где‑то их сохранить. В этом случае нужно указать доступную папку в свойстве [ImagesFolder](./).

Если папка, указанная в [ImagesFolder](./), не существует, она будет создана автоматически.

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
