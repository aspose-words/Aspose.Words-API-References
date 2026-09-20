---
title: "Aspose::Words::PageSetup::ClearFormatting метод"
linktitle: "ClearFormatting"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::ClearFormatting метод. Сбрасывает настройки страницы к размеру бумаги, полям и ориентации по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/pagesetup/clearformatting/
---
## PageSetup::ClearFormatting method


Сбрасывает настройки страницы к размерам бумаги, полям и ориентации по умолчанию.

```cpp
void Aspose::Words::PageSetup::ClearFormatting()
```


## Примеры



Показывает, как применять и отменять настройки разметки страницы для разделов в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Измените свойства разметки страницы для текущего раздела построителя и добавьте текст.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Если мы начнём новый раздел, используя построитель документа,
// он унаследует текущие свойства разметки страницы построителя.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Мы можем вернуть его свойства разметки страницы к значениям по умолчанию, используя метод "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
