---
title: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat метод"
linktitle: "get_SaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::PsSaveOptions::get_SaveFormat. Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только Ps в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только [Ps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
