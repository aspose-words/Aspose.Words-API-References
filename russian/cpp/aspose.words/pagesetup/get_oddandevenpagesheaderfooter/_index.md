---
title: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter метод"
linktitle: "get_OddAndEvenPagesHeaderFooter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter метод. Истина, если документ имеет разные колонтитулы для страниц с нечётными и чётными номерами в C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words/pagesetup/get_oddandevenpagesheaderfooter/
---
## PageSetup::get_OddAndEvenPagesHeaderFooter method


Истина, если документ имеет разные верхние и нижние колонтитулы для нечётных и чётных страниц.

```cpp
bool Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter() const
```


## Примеры



Показывает, как включить или отключить чётные колонтитулы страниц.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два типа колонтитулов.
// 1 -  "Primary" заголовок/нижний колонтитул, который отображается на каждой странице раздела.
// Мы можем переопределить основной заголовок/нижний колонтитул с помощью первого и чётного заголовка/нижнего колонтитула.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Primary header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"Primary footer.");

// 2 -  "Even" заголовок/нижний колонтитул, который появляется на каждой чётной странице этого раздела.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderEven);
builder->Writeln(u"Even page header.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterEven);
builder->Writeln(u"Even page footer.");

builder->MoveToSection(0);
builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Каждый раздел имеет объект "PageSetup", который задает свойства, связанные с внешним видом страницы
// такие как ориентация, размер и границы.
// Установите свойство "OddAndEvenPagesHeaderFooter" в значение "true"
// чтобы отображать чётный заголовок/нижний колонтитул на чётных страницах.
// Установите свойство "OddAndEvenPagesHeaderFooter" в значение "false"
// чтобы отображать основной заголовок/нижний колонтитул на чётных страницах.
builder->get_PageSetup()->set_OddAndEvenPagesHeaderFooter(oddAndEvenPagesHeaderFooter);

doc->Save(get_ArtifactsDir() + u"PageSetup.OddAndEvenPagesHeaderFooter.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
