---
title: "Метод Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName"
linktitle: "get_DocumentPartFileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName. Получает или задает имя файла (без пути), в который будет сохранена часть документа в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartfilename/
---
## DocumentPartSavingArgs::get_DocumentPartFileName method


Получает или задает имя файла (без пути), в который будет сохранена часть документа.

```cpp
System::String Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartFileName() const
```

## Примечания


Это свойство позволяет переопределить способ генерации имен файлов частей документа при экспорте в HTML или EPUB.

Когда вызывается обратный вызов, это свойство содержит имя файла, сгенерированное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить часть документа в другой файл. Обратите внимание, что имя файла для каждой части должно быть уникальным.

[DocumentPartFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name. If output document file name was not specified, for instance when saving to a stream, this file name is used only for referencing document parts. The same is true when saving to EPUB format.

## См. также

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
