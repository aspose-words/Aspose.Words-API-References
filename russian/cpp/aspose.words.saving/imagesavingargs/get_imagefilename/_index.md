---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName метод"
linktitle: "get_ImageFileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName метод. Получает или задает имя файла (без пути), в который будет сохранено изображение в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


Получает или задает имя файла (без пути), в который будет сохранено изображение.

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## Примечания


Это свойство позволяет переопределить способ генерации имен файлов изображений при экспорте в HTML.

Когда событие вызывается, это свойство содержит имя файла, сгенерированное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить изображение в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного изображения при экспорте в формат HTML. Способ генерации имени файла изображения зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла изображения выглядит как *%<document base file name>.<image number>.<extension>*.

При сохранении документа в поток сгенерированное имя файла изображения выглядит как *Aspose.Words.<document guid>.<image number>.<extension>*.

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## См. также

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
