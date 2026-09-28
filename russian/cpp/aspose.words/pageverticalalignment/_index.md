---
title: "Aspose::Words::PageVerticalAlignment перечисление"
linktitle: "PageVerticalAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageVerticalAlignment перечисление. Указывает вертикальное выравнивание текста на каждой странице в C++."
type: docs
weight: 108000
url: /ru/cpp/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enum


Указывает вертикальное выравнивание текста на каждой странице.

```cpp
enum class PageVerticalAlignment
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Низ | 3 | Текст выровнен по нижнему краю страницы. |
| По центру | 1 | Текст выровнен по центру страницы. |
| Выравнивание | 2 | Текст растягивается, чтобы заполнить страницу. |
| Верх | 0 | Текст выравнивается по верхнему краю страницы. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
