---
title: "Перечисление Aspose::Words::BreakType"
linktitle: "BreakType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BreakType enum. Указывает тип разрыва внутри документа в C++."
type: docs
weight: 82000
url: /ru/cpp/aspose.words/breaktype/
---
## BreakType enum


Указывает тип разрыва внутри документа.

```cpp
enum class BreakType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| ParagraphBreak | 0 | Разрыв между абзацами. |
| PageBreak | 1 | Явный разрыв страницы. |
| ColumnBreak | 2 | Явный разрыв колонки. |
| SectionBreakContinuous | 3 | Указывает начало новой секции на той же странице, что и предыдущая секция. |
| SectionBreakNewColumn | 4 | Указывает начало новой секции в новой колонке. |
| SectionBreakNewPage | 5 | Указывает начало новой секции на новой странице. |
| SectionBreakEvenPage | 6 | Указывает начало новой секции на новой четной странице. |
| SectionBreakOddPage | 7 | Указывает начало новой секции на нечётной странице. |
| LineBreak | 8 | Явный разрыв строки. |


## Примеры



Показывает, как вставить оглавление (TOC) в документ, используя стили заголовков в качестве записей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте оглавление для первой страницы документа.
// Настройте оглавление так, чтобы оно включало абзацы с заголовками уровней от 1 до 3.
// Также установите, чтобы его записи были гиперссылками, которые перенесут нас
// к месту заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Заполните оглавление, добавив абзацы со стилями заголовков.
// Каждый такой заголовок уровня от 1 до 3 создаст запись в оглавлении.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Оглавление — это поле типа, которое необходимо обновлять, чтобы отобразить актуальный результат.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


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
