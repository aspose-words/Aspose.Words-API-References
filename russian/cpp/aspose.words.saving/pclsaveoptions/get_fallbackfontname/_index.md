---
title: "метод Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName"
linktitle: "get_FallbackFontName"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName. Имя шрифта, который будет использоваться, если ожидаемый шрифт не найден в принтере и в коллекциях встроенных шрифтов в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


Имя шрифта, который будет использоваться, если ожидаемый шрифт не найден в принтере и в коллекциях встроенных шрифтов.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## Примеры



Показывает, как объявить шрифт, который принтер будет применять к печатному тексту в качестве замены, если оригинальный шрифт недоступен.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// Этот документ укажет принтеру применять "Times New Roman" к тексту с отсутствующим шрифтом.
// Если "Times New Roman" также недоступен, принтер по умолчанию использует шрифт "Arial".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## См. также

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
