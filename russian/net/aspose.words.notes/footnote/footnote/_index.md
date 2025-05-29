---
title: Footnote
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words для .NET
description: Создавайте привлекательные сноски без усилий с помощью нашего конструктора сносок. Повысьте ясность и профессионализм своего контента всего за несколько кликов!
type: docs
weight: 10
url: /ru/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Инициализирует экземпляр[`Footnote`](../) класс.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| footnoteType | FootnoteType | А[`FootnoteType`](../footnotetype/) value , указывающее, является ли это сноской или концевой сноской. |

## Примечания

Когда[`Footnote`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../../aspose.words/node/parentnode/) является`нулевой`.

Чтобы добавить[`Footnote`](../) к использованию документа[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) или[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) в абзаце, куда вы хотите вставить сноску.

## Примеры

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
