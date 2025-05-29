---
title: ComparisonTargetType Enum
linktitle: ComparisonTargetType
articleTitle: ComparisonTargetType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words ComparisonTargetType для точного сравнения документов. Легко настройте базовый документ для точных результатов. Начните оптимизацию прямо сейчас!
type: docs
weight: 480
url: /ru/net/aspose.words.comparing/comparisontargettype/
---
## ComparisonTargetType enumeration

Позволяет указать базовый документ, который будет использоваться при сравнении. Значение по умолчанию:Current .

```csharp
public enum ComparisonTargetType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Current | `0` | Этот документ используется в качестве основы при сравнении. |
| New | `1` | При сравнении в качестве основы используется другой документ. |

## Примечания

Относится к параметру Microsoft Word «Показать изменения в» в диалоговом окне «Сравнить документы».

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
