---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.ControlChar для эффективного управления управляющими символами в документах для улучшения форматирования и удобства чтения.
type: docs
weight: 550
url: /ru/net/aspose.words/controlchar/
---
## ControlChar class

Управляющие символы, часто встречающиеся в документах.

Чтобы узнать больше, посетите[Работа с управляющими символами](https://docs.aspose.com/words/net/working-with-control-characters/) документальная статья.

```csharp
public static class ControlChar
```

## Поля

| Имя | Описание |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | Символ конца ячейки таблицы или конца строки таблицы: "\x0007" или "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | Символ конца ячейки таблицы или конца строки таблицы: (char)7 или "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | Символ конца столбца: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | Символ конца столбца: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | Символ возврата каретки: "\x000d" или "\r". То же, что и[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | Возврат каретки, за которым следует символ перевода строки: "\x000d\x000a" или "\r\n". Не используется как таковой в документах Microsoft Word, но обычно используется в текстовых файлах для разрывов абзацев. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | Это символ «o», используемый в качестве значения по умолчанию в полях формы ввода текста. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | Конец символа поля MS Word: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | Символ-разделитель полей отделяет код поля от значения поля. Необязательно в некоторых полях. Значение: (char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | Начало символа поля MS Word: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | Символ перевода строки: "\x000a" или "\n". То же, что и[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | Символ переноса строки: "\x000b" или "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | Символ переноса строки: (char)11 или "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | Символ перевода строки: "\x000a" или "\n". То же, что и[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | Символ перевода строки: (char)10 или "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | Неразрывный дефис в Microsoft Word — (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | Неразрывный пробел: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | Неразрывный пробел: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | Необязательный дефис в Microsoft Word — (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | Символ разрыва страницы: "\x000c" или "\f". Обратите внимание, что он имеет то же значение, что и[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | Символ разрыва страницы: (char)12 или "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | Символ конца абзаца: "\x000d" или "\r". То же, что[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | Символ конца абзаца: (char)13 или "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | Символ конца раздела: "\x000c" или "\f". Обратите внимание, что он имеет то же значение, что и[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | Символ конца раздела: (char)12 или "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | Символ пробела: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | Символ табуляции: "\x0009" или "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | Символ табуляции: (char)9 или "\t". |

## Примечания

Предоставляет как символьные, так и строковые версии одних и тех же констант. Например: string[`LineBreak`](./linebreak/) и чар[`LineBreakChar`](./linebreakchar/) имеют одинаковое значение.

## Примеры

Показывает, как использовать управляющие символы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте абзацы с текстом с помощью DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Преобразование документа в текстовую форму показывает, что управляющие символы
// представляют некоторые структурные элементы документа, такие как разрывы страниц.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// При преобразовании документа в строковую форму,
// мы можем опустить некоторые управляющие символы с помощью метода Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
