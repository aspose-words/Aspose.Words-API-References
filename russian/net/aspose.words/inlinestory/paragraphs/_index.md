---
title: InlineStory.Paragraphs
second_title: Справочник по API Aspose.Words для .NET
description: InlineStory свойство. Получает набор абзацев которые являются непосредственными дочерними элементами статьи.
type: docs
weight: 80
url: /ru/net/aspose.words/inlinestory/paragraphs/
---
## InlineStory.Paragraphs property

Получает набор абзацев, которые являются непосредственными дочерними элементами статьи.

```csharp
public ParagraphCollection Paragraphs { get; }
```

### Примеры

Показывает, как добавить комментарий к абзацу.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

// В Microsoft Word мы можем щелкнуть правой кнопкой мыши этот комментарий в теле документа, чтобы отредактировать его или ответить на него. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Показывает, как вставлять и настраивать сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем текст и ссылаемся на него сноской. Эта сноска поместит небольшую ссылку в верхнем индексе
// отметить после текста, на который он ссылается, и создать запись под основным текстом в нижней части страницы.
// Эта запись будет содержать отметку сноски и текст ссылки,
// который мы передадим методу "InsertFootnote" конструктора документов.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Если для этого свойства задано значение "true", то референтная метка нашей сноски
// будет его индексом среди всех сносок раздела.
// Это первая сноска, поэтому ссылочным знаком будет "1".
Assert.True(footnote.IsAuto);

// Мы можем переместить конструктор документа внутрь сноски, чтобы отредактировать его ссылочный текст. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Мы можем установить пользовательскую отметку, которую сноска будет использовать вместо своего порядкового номера.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Закладка с флагом "IsAuto", установленным в true, по-прежнему будет показывать свой реальный индекс
// даже если предыдущие закладки отображают пользовательские метки ссылок, метка этой закладки будет "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Смотрите также

* class [ParagraphCollection](../../paragraphcollection/)
* class [InlineStory](../)
* пространство имен [Aspose.Words](../../inlinestory/)
* сборка [Aspose.Words](../../../)


