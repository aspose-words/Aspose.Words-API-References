---
title: Compare
second_title: Справочник по API Aspose.Words для .NET
description: Сравнивает этот документ с другим документом внося изменения в виде количества редакций и форматирования.Revisionaspose.words/revision .
type: docs
weight: 540
url: /ru/net/aspose.words/document/compare/
---
## Compare(Document, string, DateTime) {#compare}

Сравнивает этот документ с другим документом, внося изменения в виде количества редакций и форматирования.[`Revision`](../../revision) .

```csharp
public void Compare(Document document, string author, DateTime dateTime)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Документ для сравнения. |
| author | String | Инициалы автора использовать для редакций. |
| dateTime | DateTime | Дата и время для использования для изменений. |

### Примечания

На данный момент не сравниваются следующие узлы документа:

* [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag)
* Пункт 3

Документы не должны иметь редакций перед сравнением.

### Примеры

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

// После сравнения исходный документ получит новую ревизию
// для каждого отличающегося элемента в редактируемом документе.
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

// Принятие этих изменений преобразует исходный документ в отредактированный документ.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Смотрите также

* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
* сборка [Aspose.Words](../../../)

---

## Compare(Document, string, DateTime, CompareOptions) {#compare_1}

Сравнивает этот документ с другим документом, внося изменения в виде количества редакций и форматирования.[`Revision`](../../revision) . Позволяет указать параметры сравнения, используя[`CompareOptions`](../../../aspose.words.comparing/compareoptions) .

```csharp
public void Compare(Document document, string author, DateTime dateTime, CompareOptions options)
```

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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions)
* class [Document](../../document)
* пространство имен [Aspose.Words](../../document)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
