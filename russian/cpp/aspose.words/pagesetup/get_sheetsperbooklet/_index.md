---
title: "Aspose::Words::PageSetup::get_SheetsPerBooklet метод"
linktitle: "get_SheetsPerBooklet"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_SheetsPerBooklet метод. Возвращает или задает количество страниц, включаемых в каждый буклет, в C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words/pagesetup/get_sheetsperbooklet/
---
## PageSetup::get_SheetsPerBooklet method


Возвращает или задает количество страниц, включаемых в каждый буклет.

```cpp
int32_t Aspose::Words::PageSetup::get_SheetsPerBooklet() const
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
