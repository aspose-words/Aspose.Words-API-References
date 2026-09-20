---
title: "Метод Aspose::Words::PageSetup::get_MultiplePages"
linktitle: "get_MultiplePages"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_MultiplePages. Для многостраничных документов получает или задает способ печати или рендеринга документа, чтобы его можно было собрать в виде брошюры в C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words/pagesetup/get_multiplepages/
---
## PageSetup::get_MultiplePages method


Для многостраничных документов получает или задает способ печати или отображения документа, чтобы его можно было собрать в виде брошюры.

```cpp
Aspose::Words::Settings::MultiplePagesType Aspose::Words::PageSetup::get_MultiplePages() const
```


## Примеры



Показывает, как установить поля канвы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Вставьте текст, который охватывает несколько страниц.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Канва добавляет пробелы к левому или правому полю страницы,
// что компенсирует центральное сгибание страниц в книге, вторгающееся в макет страницы.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Определите, сколько места наши страницы имеют для текста внутри полей, а затем добавьте значение для заполнения поля.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Установите свойство "RtlGutter" в "true", чтобы разместить канву в более подходящем положении для текста справа налево.
pageSetup->set_RtlGutter(true);

// Установите свойство "MultiplePages" в "MultiplePagesType.MirrorMargins", чтобы чередовать
// позицию левого/правого края полей на каждой странице.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```


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

* Enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
