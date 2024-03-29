---
title: Footnote.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words для .NET
description: Footnote StoryType свойство. ВозвращаетFootnotes илиEndnotes  на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.notes/footnote/storytype/
---
## Footnote.StoryType property

ВозвращаетFootnotes илиEndnotes .

```csharp
public override StoryType StoryType { get; }
```

## Примеры

Показывает, как вставлять узлы InlineStory.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Узлы таблицы имеют метод EnsureMinimum(), который гарантирует, что в таблице есть хотя бы одна ячейка.
Table table = new Table(doc);
table.EnsureMinimum();

// Мы можем поместить таблицу внутри сноски, после чего она появится в нижнем колонтитуле ссылающейся страницы.
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// InlineStory также имеет метод EnsureMinimum(), но в данном случае
// он гарантирует, что последний дочерний элемент узла является абзацем,
// чтобы мы могли легко щелкать мышью и писать текст в Microsoft Word.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Редактируем внешний вид привязки, которая представляет собой небольшой номер надстрочного индекса
// в основном тексте, указывающем на сноску.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Все узлы встроенных историй имеют соответствующие типы историй.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Комментарий — это еще один тип встроенной истории.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Родительским абзацем встроенного узла истории будет абзац из основного тела документа.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Однако последний абзац — это текст содержимого комментария,
// который будет находиться за пределами основного тела документа в речевом пузыре.
// Комментарий по умолчанию не будет иметь дочерних узлов,
// поэтому мы можем применить метод обеспеченияМинимум(), чтобы разместить здесь абзац.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Когда у нас есть абзац, мы можем переместить его в конструктор и написать комментарий.
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
