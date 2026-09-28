---
title: "Aspose::Words::ControlChar класс"
linktitle: "ControlChar"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ControlChar класс. Управляющие символы часто встречаются в документах. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words/controlchar/
---
## ControlChar class


Управляющие символы, часто встречающиеся в документах. Чтобы узнать больше, посетите статью документации [Working With Control Characters](https://docs.aspose.com/words/cpp/working-with-control-characters/).

```cpp
class ControlChar
```

## Методы

| Метод | Описание |
| --- | --- |
| static [Cell](./cell/)() | Символ конца ячейки таблицы или конца строки таблицы: "\x0007" или "\a". |
| static [ColumnBreak](./columnbreak/)() | Символ конца столбца: "\x000e". |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | Символ возврата каретки: "\x000d" или "\r". То же, что и [ParagraphBreak](./paragraphbreak/). |
| static [CrLf](./crlf/)() | Символ возврата каретки, за которым следует перевод строки: "\x000d\x000a" или "\r\n". Не используется так в документах Microsoft Word, но часто применяется в текстовых файлах для разрывов абзацев. |
| static [Lf](./lf/)() | Символ перевода строки: "\x000a" или "\n". То же, что и [LineFeed](./linefeed/). |
| static [LineBreak](./linebreak/)() | Символ разрыва строки: "\x000b" или "\v". |
| static [LineFeed](./linefeed/)() | Символ перевода строки: "\x000a" или "\n". То же, что и [Lf](./lf/). |
| static [NonBreakingSpace](./nonbreakingspace/)() | Символ неразрывного пробела: "\x00a0". |
| static [PageBreak](./pagebreak/)() | Символ разрыва страницы: "\x000c" или "\f". Обратите внимание, что он имеет то же значение, что и [SectionBreak](./sectionbreak/). |
| static [ParagraphBreak](./paragraphbreak/)() | Символ конца абзаца: "\x000d" или "\r". То же, что и [Cr](./cr/) |
| static [SectionBreak](./sectionbreak/)() | Символ конца раздела: "\x000c" или "\f". Обратите внимание, что он имеет то же значение, что и [PageBreak](./pagebreak/). |
| static [Tab](./tab/)() | Символ табуляции: "\x0009" или "\t". |
## Поля

| Поле | Описание |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | Символ конца ячейки таблицы или конца строки таблицы: (char)7 или "\a". |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | Символ конца столбца: (char)14. |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | Это символ "o", используемый в качестве значения по умолчанию в полях ввода текста формы. |
| static constexpr [FieldEndChar](./fieldendchar/) | Символ конца поля MS Word: (char)21. |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | Символ-разделитель поля разделяет код поля и значение поля. Необязательно в некоторых полях. Значение: (char)20. |
| static constexpr [FieldStartChar](./fieldstartchar/) | Символ начала поля MS Word: (char)19. |
| static constexpr [LineBreakChar](./linebreakchar/) | Символ разрыва строки: (char)11 или "\v". |
| static constexpr [LineFeedChar](./linefeedchar/) | Символ перевода строки: (char)10 или "\n". |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | Неразрывный дефис в Microsoft Word имеет код (char)30. |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | Неразрывный пробел: (char)160. |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | Опциональный дефис в Microsoft Word имеет код (char)31. |
| static constexpr [PageBreakChar](./pagebreakchar/) | Символ разрыва страницы: (char)12 или "\f". |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | Символ конца абзаца: (char)13 или "\r". |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | Символ конца раздела: (char)12 или "\f". |
| static constexpr [SpaceChar](./spacechar/) | Символ пробела: (char)32. |
| static constexpr [TabChar](./tabchar/) | Символ табуляции: (char)9 или "\t". |

## Примеры



Показывает, как использовать управляющие символы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставка абзацев с текстом с помощью DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Преобразование документа в текстовый вид показывает, что управляющие символы
// представляют некоторые структурные элементы документа, такие как разрывы страниц.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// При преобразовании документа в строковый вид,
// мы можем опустить некоторые управляющие символы с помощью метода Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
