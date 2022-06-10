---
title: CompareOptions
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет выбрать дополнительные параметры операции сравнения документов.
type: docs
weight: 260
url: /ru/net/aspose.words.comparing/compareoptions/
---
## CompareOptions class

Позволяет выбрать дополнительные параметры операции сравнения документов.

```csharp
public class CompareOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CompareOptions](compareoptions)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Granularity](../../aspose.words.comparing/compareoptions/granularity) { get; set; } | Указывает, отслеживаются ли изменения по символам или по словам. Значение по умолчанию:WordLevel. |
| [IgnoreCaseChanges](../../aspose.words.comparing/compareoptions/ignorecasechanges) { get; set; } | True указывает, что сравнение документов нечувствительно к регистру. По умолчанию сравнение чувствительно к регистру. |
| [IgnoreComments](../../aspose.words.comparing/compareoptions/ignorecomments) { get; set; } | Указывает, следует ли сравнивать различия в комментариях. По умолчанию комментарии не игнорируются. |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/compareoptions/ignoredmluniqueid) { get; set; } | Указывает, следует ли игнорировать разницу в уникальном идентификаторе DrawingML. Значение по умолчанию: **false** . |
| [IgnoreFields](../../aspose.words.comparing/compareoptions/ignorefields) { get; set; } | Указывает, следует ли сравнивать различия в полях. По умолчанию поля не игнорируются. |
| [IgnoreFootnotes](../../aspose.words.comparing/compareoptions/ignorefootnotes) { get; set; } | Указывает, следует ли сравнивать различия в сносках и концевых сносках. По умолчанию сноски не игнорируются. |
| [IgnoreFormatting](../../aspose.words.comparing/compareoptions/ignoreformatting) { get; set; } | True указывает, что форматирование игнорируется. По умолчанию форматирование документа не игнорируется. |
| [IgnoreHeadersAndFooters](../../aspose.words.comparing/compareoptions/ignoreheadersandfooters) { get; set; } | True указывает, что содержимое верхних и нижних колонтитулов игнорируется. По умолчанию верхние и нижние колонтитулы не игнорируются. |
| [IgnoreTables](../../aspose.words.comparing/compareoptions/ignoretables) { get; set; } | Указывает, следует ли сравнивать различия в данных, содержащихся в таблицах. По умолчанию таблицы не игнорируются. |
| [IgnoreTextboxes](../../aspose.words.comparing/compareoptions/ignoretextboxes) { get; set; } | Указывает, следует ли сравнивать различия в данных, содержащихся в текстовых полях. По умолчанию текстовые поля не игнорируются. |
| [Target](../../aspose.words.comparing/compareoptions/target) { get; set; } | Указывает, какой документ будет использоваться в качестве эталона при сравнении. |

### Примеры

Показывает, как фильтровать определенные типы элементов документа при сравнении.

```csharp
// Создайте исходный документ и заполните его различными элементами.
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

// Сравнение документов создает ревизию для каждой правки в редактируемом документе.
// Объект CompareOptions имеет ряд флагов, которые могут подавлять ревизии
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

* namespace [Aspose.Words.Comparing](../../aspose.words.comparing)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
