---
title: Footnote.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Footnote StoryType, чтобы легко получать доступ к сноскам или концевым сноскам, повышая ясность и глубину вашего контента для читателей.
type: docs
weight: 70
url: /ru/net/aspose.words.notes/footnote/storytype/
---
## Footnote.StoryType property

ВозвратFootnotes илиEndnotes .

```csharp
public override StoryType StoryType { get; }
```

## Примеры

Показывает, как вставлять узлы InlineStory.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Узлы таблицы имеют метод «EnsureMinimum()», который гарантирует, что в таблице есть хотя бы одна ячейка.
Table table = new Table(doc);
table.EnsureMinimum();

// Мы можем поместить таблицу в сноску, и она появится в нижнем колонтитуле ссылающейся страницы.
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// InlineStory также имеет метод "EnsureMinimum()", но в этом случае
// он гарантирует, что последний дочерний элемент узла является абзацем,
// чтобы мы могли легко набирать текст в Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Отредактируйте внешний вид якоря, представляющего собой маленькую надстрочную цифру
// в основном тексте, указывающем на сноску.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Все встроенные узлы историй имеют соответствующие им типы историй.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Комментарий — это еще один тип встроенной истории.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Родительским абзацем встроенного узла истории будет абзац из основного текста документа.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Однако последний абзац — это текст комментария,
// который будет находиться за пределами основного текста документа в речевом пузыре.
// По умолчанию комментарий не будет иметь дочерних узлов,
// поэтому мы можем применить метод EnsureMinimum(), чтобы разместить здесь абзац.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Как только у нас есть абзац, мы можем переместить конструктор, чтобы он сделал это, и написать наш комментарий.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Смотрите также

* enum [StoryType](../../../aspose.words/storytype/)
* class [Footnote](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
