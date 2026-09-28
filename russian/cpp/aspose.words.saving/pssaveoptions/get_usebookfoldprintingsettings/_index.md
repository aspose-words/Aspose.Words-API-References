---
title: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings метод"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings. Получает или задаёт логическое значение, указывающее, следует ли сохранять документ с использованием книжной печати, если это указано через MultiplePages в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/pssaveoptions/get_usebookfoldprintingsettings/
---
## PsSaveOptions::get_UseBookFoldPrintingSettings method


Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием книжной раскладки печати, если она указана через [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Примечания


Если эта опция указана, [PageSet](../../fixedpagesaveoptions/get_pageset/) игнорируется при сохранении. Такое поведение соответствует MS Word. Если настройки книжной печати не указаны в настройках страницы, эта опция не будет иметь эффекта.

## Примеры



Показывает, как сохранить документ в формате Postscript в виде книжного сгиба.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Создайте объект \"PsSaveOptions\", который мы можем передать методу \"Save\" документа
// чтобы изменить способ, которым этот метод преобразует документ в PostScript.
// Установите свойство \"UseBookFoldPrintingSettings\" в значение \"true\", чтобы расположить содержимое
// в выходном документе Postscript таким образом, чтобы создать из него буклет.
// Установите свойство \"UseBookFoldPrintingSettings\" в значение \"false\", чтобы сохранить документ обычным способом.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Если мы рендерим документ как буклет, мы должны установить \"MultiplePages\"
// свойства объектов настройки страницы всех разделов в "MultiplePagesType.BookFoldPrinting".
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// Как только мы распечатаем этот документ с обеих сторон листов, мы сможем сложить все листы пополам одновременно,
// и содержимое выровняется таким образом, что получится брошюра.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## См. также

* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
