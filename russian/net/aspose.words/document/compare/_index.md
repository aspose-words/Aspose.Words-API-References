---
title: Document.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words для .NET
description: Легко сравнивайте документы с помощью нашего инструмента сравнения документов. Быстро определяйте правки и изменения формата для упрощения редактирования и улучшения совместной работы.
type: docs
weight: 600
url: /ru/net/aspose.words/document/compare/
---
## Compare(*[Document](../), string, DateTime*) {#compare}

Сравнивает этот документ с другим документом, внося изменения по количеству правок и редакций формата[`Revision`](../../revision/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Документ для сравнения. |
| author | String | Инициалы автора для использования при исправлениях. |
| dateTime | DateTime | Дата и время, которые следует использовать для внесения изменений. |

## Примечания

Перед сравнением документы не должны иметь изменений.

## Примеры

Показывает, как сравнивать документы.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Сравнение документов с ревизиями вызовет исключение.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

// После сравнения исходный документ получит новую версию
// для каждого элемента, отличающегося в редактируемом документе.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Принятие этих изменений преобразует исходный документ в отредактированный документ.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Compare(*[Document](../), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Сравнивает этот документ с другим документом, внося изменения в виде ряда правок и редакций формата[`Revision`](../../revision/) . Позволяет указать параметры сравнения с помощью[`CompareOptions`](../../../aspose.words.comparing/compareoptions/) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
