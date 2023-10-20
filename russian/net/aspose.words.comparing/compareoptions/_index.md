---
title: CompareOptions Class
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words для .NET
description: Aspose.Words.Comparing.CompareOptions сорт. Позволяет выбрать дополнительные параметры для операции сравнения документов на С#.
type: docs
weight: 270
url: /ru/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Позволяет выбрать дополнительные параметры для операции сравнения документов.

Чтобы узнать больше, посетите[Сравнить документы](https://docs.aspose.com/words/net/compare-documents/) статья документации.

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
| [CompareMoves](../../aspose.words.comparing/compareoptions/comparemoves/) { get; set; } | Указывает, сравнивать ли различия вMoveRevision между двумя документами. По умолчанию изменения перемещения не создаются. |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity/) { get; set; } | Указывает, отслеживаются ли изменения посимвольно или пословно. Значение по умолчанию:WordLevel . |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges/) { get; set; } | True указывает, что сравнение документов выполняется без учета регистра. По умолчанию сравнение выполняется с учетом регистра. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments/) { get; set; } | Указывает, сравнивать ли различия в комментариях. По умолчанию комментарии не игнорируются. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid/) { get; set; } | Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML. Значение по умолчанию:`ЛОЖЬ` . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields/) { get; set; } | Указывает, следует ли сравнивать различия в полях. По умолчанию поля не игнорируются. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes/) { get; set; } | Указывает, следует ли сравнивать различия в сносках и концевых сносках. По умолчанию сноски не игнорируются. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting/) { get; set; } | True указывает, что форматирование игнорируется. По умолчанию форматирование документа не игнорируется. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters/) { get; set; } | True указывает, что содержимое верхних и нижних колонтитулов игнорируется. По умолчанию верхние и нижние колонтитулы не игнорируются. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables/) { get; set; } | Указывает, следует ли сравнивать различия в данных, содержащихся в таблицах. По умолчанию таблицы не игнорируются. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes/) { get; set; } | Указывает, следует ли сравнивать различия в данных, содержащихся в текстовых полях. По умолчанию текстовые поля не игнорируются. |
| [Target](../../aspose.words.comparing/compareoptions/target/) { get; set; } | Указывает, какой документ будет использоваться в качестве целевого при сравнении. |

## Примеры

Показывает, как фильтровать определенные типы элементов документа при сравнении.

```csharp
// Создаем исходный документ и заполняем его различными элементами.
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);

// Текст абзаца, на который есть сноска:
builder.Writeln("Hello world! This is the first paragraph.");
builder.InsertFootnote(FootnoteType.Endnote, "Original endnote text.");

// Стол:
builder.StartTable();
builder.InsertCell();
builder.Write("Original cell 1 text");
builder.InsertCell();
builder.Write("Original cell 2 text");
builder.EndTable();

// Текстовое окно:
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

// Создаем клон нашего документа и быстро редактируем каждый из элементов клонированного документа.
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

// При сравнении документов создается редакция для каждого изменения в редактируемом документе.
// Объект CompareOptions имеет ряд флагов, которые могут подавлять изменения
// для каждого соответствующего типа элемента, фактически игнорируя их изменение.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreFormatting = false;
compareOptions.IgnoreCaseChanges = false;
compareOptions.IgnoreComments = false;
compareOptions.IgnoreTables = false;
compareOptions.IgnoreFields = false;
compareOptions.IgnoreFootnotes = false;
compareOptions.IgnoreTextboxes = false;
compareOptions.IgnoreHeadersAndFooters = false;
compareOptions.Target = ComparisonTargetType.New;

docOriginal.Compare(docEdited, "John Doe", DateTime.Now, compareOptions);
docOriginal.Save(ArtifactsDir + "Document.CompareOptions.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Comparing](../../aspose.words.comparing/)
* сборка [Aspose.Words](../../)
