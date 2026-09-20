---
title: "Метод Aspose::Words::Saving::PclSaveOptions::AddPrinterFont"
linktitle: "AddPrinterFont"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::PclSaveOptions::AddPrinterFont. Добавляет информацию о шрифте, который загружается в принтер производителем, в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


Добавляет информацию о шрифте, загружаемом в принтер производителем.

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFullName | const System::String\& | Полное название шрифта (например, "Times New Roman Bold Italic"). |
| fontPclName | const System::String\& | Название шрифта, используемого в документе Pcl. |

## Примеры



Показывает, как заставить принтер заменить все вхождения определённого шрифта другим шрифтом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// При печати этого документа принтер будет использовать шрифт "Courier New"
// чтобы обратиться к местам, где наш документ использовал шрифт "Courier".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## См. также

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
