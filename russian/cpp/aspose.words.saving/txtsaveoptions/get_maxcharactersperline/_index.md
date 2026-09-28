---
title: "Метод Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine"
linktitle: "get_MaxCharactersPerLine"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine. Получает или задает целочисленное значение, указывающее максимальное количество символов в одной строке. Значение по умолчанию — 0, что означает отсутствие ограничения в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


Получает или задаёт целочисленное значение, указывающее максимальное количество символов в одной строке. Значение по умолчанию — 0, что означает отсутствие ограничения.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## Примеры



Показывает, как установить максимальное количество символов в строке.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Установите 30 символов как максимальное допустимое количество в одной строке.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## См. также

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
