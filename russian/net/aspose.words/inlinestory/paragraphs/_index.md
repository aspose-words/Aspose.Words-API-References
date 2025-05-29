---
title: InlineStory.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words для .NET
description: Откройте для себя свойство InlineStory Paragraphs, получите доступ к уникальной коллекции абзацев истории для улучшенной организации контента и удобства чтения.
type: docs
weight: 80
url: /ru/net/aspose.words/inlinestory/paragraphs/
---
## InlineStory.Paragraphs property

Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории.

```csharp
public ParagraphCollection Paragraphs { get; }
```

## Примеры

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

 // В Microsoft Word мы можем щелкнуть правой кнопкой мыши этот комментарий в тексте документа, чтобы отредактировать его или ответить на него.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Показывает, как вставлять и настраивать сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте текст и сделайте на него ссылку с помощью сноски. Эта сноска поместит небольшую надстрочную ссылку
// отметьте после текста, на который он ссылается, и создайте запись под основным текстом в нижней части страницы.
// Эта запись будет содержать ссылочный знак сноски и текст ссылки,
// который мы передадим методу "InsertFootnote" конструктора документа.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Если это свойство установлено в значение "true", то ссылочный знак нашей сноски
// будет его индексом среди всех сносок раздела.
// Это первая сноска, поэтому ссылочный знак будет «1».
Assert.True(footnote.IsAuto);

 // Мы можем переместить конструктор документа внутрь сноски, чтобы редактировать ее ссылочный текст.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Мы можем установить пользовательский ссылочный знак, который будет использоваться в сноске вместо ее индексного номера.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Закладка с флагом "IsAuto", установленным в значение true, по-прежнему будет отображать свой реальный индекс
// даже если предыдущие закладки отображали пользовательские контрольные метки, контрольная метка этой закладки будет «3».
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Смотрите также

* class [ParagraphCollection](../../paragraphcollection/)
* class [InlineStory](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
