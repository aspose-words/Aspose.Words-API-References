---
title: "Метод Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName"
linktitle: "get_ResourceFileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName. Получает или задает имя файла (без пути), в который будет сохранён ресурс в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


Получает или задает имя файла (без пути), в который будет сохранён ресурс.

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## Примечания


Это свойство позволяет переопределить способ генерации имён файлов ресурсов при экспорте в фиксированный HTML, SVG или Markdown.

Когда событие вызывается, это свойство содержит имя файла, сгенерированное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить ресурс в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого ресурса при экспорте в фиксированный HTML, SVG или Markdown. Способ генерации имени файла ресурса зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла ресурса выглядит как *%<document base file name>.<image number>.<extension>*.

При сохранении документа в поток сгенерированное имя файла ресурса выглядит как *Aspose.Words.<document guid>.<image number>.<extension>*.

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## См. также

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
