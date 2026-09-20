---
title: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings метод"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings метод. Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием книжной раскладки печати, если она указана через MultiplePages в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием книжной раскладки печати, если она указана через [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Примечания


Если эта опция указана, [PageSet](../../fixedpagesaveoptions/get_pageset/) игнорируется при сохранении. Такое поведение соответствует MS Word. Если настройки книжной печати не указаны в настройках страницы, эта опция не будет иметь эффекта.

## Примеры



Показывает, как сохранить документ в формате XPS в виде книжного сгиба.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Создайте объект \"XpsSaveOptions\" объект, который мы можем передать методу \"Save\" документа
// чтобы изменить способ, которым этот метод преобразует документ в .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// Установите свойство \"UseBookFoldPrintingSettings\" в значение \"true\", чтобы расположить содержимое
// в выходном XPS таким образом, чтобы мы могли использовать его для создания брошюры.
// Установите свойство "UseBookFoldPrintingSettings" в "false", чтобы отрисовать XPS нормально.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// Если мы рендерим документ как буклет, мы должны установить \"MultiplePages\"
// свойства объектов настройки страницы всех разделов в "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// После печати этого документа мы можем превратить его в брошюру, сложив страницы
// выходить из принтера и складываться пополам.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## См. также

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
