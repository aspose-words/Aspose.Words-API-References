---
title: "Aspose::Words::Settings::MultiplePagesType enum"
linktitle: "MultiplePagesType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::MultiplePagesType enum. Указывает, как документ выводится при печати в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enum


Указывает, как документ выводится на печать.

```cpp
enum class MultiplePagesType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Обычный | 0 | Обычная печать, без указания нескольких страниц. |
| MirrorMargins | 1 | Меняет местами левый и правый поля на соседних страницах. |
| TwoPagesPerSheet | 2 | Печатает две страницы на листе. |
| BookFoldPrinting | 3 | Указывает, следует ли печатать документ в виде книжного сгиба. |
| BookFoldPrintingReverse | 4 | Указывает, следует ли печатать документ в виде обратного книжного сгиба. |
| Default | n/a | Значение по умолчанию — [Normal](./) |


## Примеры



Показывает, как настроить документ, который можно печатать в виде книжного сгиба.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте текст, охватывающий 16 страниц.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Настройте свойство "PageSetup" первой секции, чтобы печатать документ в виде книжного сгиба.
// Когда мы печатаем этот документ с двух сторон, мы можем взять страницы, чтобы сложить их в стопку
// и сложить их все одновременно пополам. Содержание документа выровняется в книжный сгиб.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Мы можем указывать количество листов только кратным 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
