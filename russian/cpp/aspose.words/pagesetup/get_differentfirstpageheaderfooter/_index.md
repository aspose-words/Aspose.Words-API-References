---
title: "Метод Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter"
linktitle: "get_DifferentFirstPageHeaderFooter"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter. Возвращает true, если на первой странице используется иной заголовок или нижний колонтитул в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words/pagesetup/get_differentfirstpageheaderfooter/
---
## PageSetup::get_DifferentFirstPageHeaderFooter method


Истина, если на первой странице используется другой верхний или нижний колонтитул.

```cpp
bool Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter()
```


## Примеры



Показывает, как включить или отключить основные заголовки/нижние колонтитулы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два типа колонтитулов.
// 1 -  "First" заголовок/нижний колонтитул, который отображается на первой странице раздела.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderFirst);
builder->Writeln(u"First page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterFirst);
builder->Writeln(u"First page footer.");

// 2 -  "Primary" заголовок/нижний колонтитул, который отображается на каждой странице раздела.
// Мы можем переопределить основной заголовок/нижний колонтитул с помощью первого и чётного заголовка/нижнего колонтитула.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Каждый раздел имеет объект "PageSetup", который задает свойства, связанные с внешним видом страницы
// такие как ориентация, размер и границы.
// Установите свойство "DifferentFirstPageHeaderFooter" в "true", чтобы применить первый заголовок/нижний колонтитул к первой странице.
// Установите свойство "DifferentFirstPageHeaderFooter" в "false"
// чтобы первая страница отображала основной заголовок/нижний колонтитул.
builder->get_PageSetup()->set_DifferentFirstPageHeaderFooter(differentFirstPageHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.DifferentFirstPageHeaderFooter.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
