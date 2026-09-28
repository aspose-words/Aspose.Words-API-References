---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName метод"
linktitle: "get_FontFileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName метод. Получает или задает имя файла (без пути), в который будет сохранён шрифт в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


Получает или задает имя файла (без пути), в который будет сохранён шрифт.

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## Примечания


Это свойство позволяет переопределить способ генерации имён файлов шрифтов при экспорте в HTML.

Когда событие вызывается, это свойство содержит имя файла, сгенерированное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить шрифт в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного шрифта при экспорте в формат HTML. Способ генерации имени файла шрифта зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла шрифта выглядит как *%<document base file name>.<original file name><optional suffix>.<extension>*.

При сохранении документа в поток сгенерированное имя файла шрифта выглядит как *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>*.

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## См. также

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
