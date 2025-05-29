---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.CompareOptions для расширенного сравнения документов. Настройте параметры сравнения для точных результатов и повышения производительности.
type: docs
weight: 470
url: /ru/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Позволяет выбрать дополнительные параметры для операции сравнения документов.

Чтобы узнать больше, посетите[Сравнить документы](https://docs.aspose.com/words/net/compare-documents/) документальная статья.

```csharp
public class CompareOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CompareOptions](compareoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AdvancedOptions](../../aspose.words.comparing/compareoptions/advancedoptions/) { get; } | Указывает расширенные параметры сравнения, которые могут помочь получить более точные результаты сравнения. |
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | Указывает, следует ли сравнивать различия между двумя документами. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Указывает, отслеживаются ли изменения по символам или по словам. |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True указывает, что сравнение документов нечувствительно к регистру. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Указывает, следует ли сравнивать различия в комментариях. |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Указывает, следует ли сравнивать различия в полях. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Указывает, следует ли сравнивать различия в сносках и концевых сносках. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True указывает, что форматирование игнорируется. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True указывает, что содержимое верхних и нижних колонтитулов игнорируется. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Указывает, следует ли сравнивать различия в данных, содержащихся в таблицах. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Указывает, следует ли сравнивать различия в данных, содержащихся в текстовых полях. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Указывает, какой документ будет использоваться в качестве цели при сравнении. |

## Примеры

Показывает, как фильтровать определенные типы элементов документа при сравнении.

```csharp
// Создаем исходный документ и заполняем его различными типами элементов.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Текст абзаца, на который ссылается концевая сноска:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Стол:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Текстовое поле:
Shape textBox = builder.InsertShape(ShapeType.TextBox, 150, 20);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("Original textbox contents");

// Поле ДАТА:
builder.MoveTo(docOriginal.FirstSection.Body.AppendParagraph(""));
builder.InsertField(" DATE ");

// Комментарий:
Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", DateTime.Now);
newComment.SetText("Original comment.");
builder.CurrentParagraph.AppendChild(newComment);

// Заголовок:
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Original header contents.");

// Создаем клон нашего документа и выполняем быстрое редактирование каждого из элементов клонированного документа.
Document docEdited = (Document)docOriginal.Clone(true);
Paragraph firstParagraph = docEdited.FirstSection.Body.FirstParagraph;

firstParagraph.Runs[0].Text = "hello world! this is the first paragraph, after editing.";
firstParagraph.ParagraphFormat.Style = docEdited.Styles[StyleIdentifier.Heading1];
((Footnote)docEdited.GetChild(NodeType.Footnote, 0, true)).FirstParagraph.Runs[1].Text = "Edited endnote text.";
((Table)docEdited.GetChild(NodeType.Table, 0, true)).FirstRow.Cells[1].FirstParagraph.Runs[0].Text = "Edited Cell 2 contents";
((Shape)docEdited.GetChild(NodeType.Shape, 0, true)).FirstParagraph.Runs[0].Text = "Edited textbox contents";
((FieldDate)docEdited.Range.Fields[0]).UseLunarCalendar = true;
((Comment)docEdited.GetChild(NodeType.Comment, 0, true)).FirstParagraph.Runs[0].Text = "Edited comment.";
docEdited.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].FirstParagraph.Runs[0].Text =
    "Edited header contents.";

// Сравнение документов создает ревизию для каждого изменения в редактируемом документе.
// Объект CompareOptions имеет ряд флагов, которые могут подавлять изменения
// для каждого соответствующего типа элемента, фактически игнорируя их изменения.
CompareOptions compareOptions = new CompareOptions
{
    CompareMoves = false,
    IgnoreFormatting = false,
    IgnoreCaseChanges = false,
    IgnoreComments = false,
    IgnoreTables = false,
    IgnoreFields = false,
    IgnoreFootnotes = false,
    IgnoreTextboxes = false,
    IgnoreHeadersAndFooters = false,
    Target = ComparisonTargetType.New
};

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Revision.CompareOptions.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Comparing](../../aspose.words.comparing/)
* сборка [Aspose.Words](../../)
