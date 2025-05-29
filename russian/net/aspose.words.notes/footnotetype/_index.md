---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.FootnoteType. Легко различайте сноски и концевые сноски для улучшенного форматирования и ясности документа.
type: docs
weight: 5020
url: /ru/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

Указывает, является ли это сноской или концевой сноской.

```csharp
public enum FootnoteType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Footnote | `0` | Объект — сноска. |
| Endnote | `1` | Объект является концевой сноской. |

## Примечания

Как сноски, так и концевые сноски представлены объектамиFootnote класс. Использовать[`FootnoteType`](../footnote/footnotetype/) для различения сносок и концевых сносок.

## Примеры

Показывает, как ссылаться на текст с помощью сносок и концевых сносок.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте текст и отметьте его сноской, установив свойство IsAuto в значение «true» по умолчанию,
// поэтому маркер, видимый в основном тексте, будет автоматически пронумерован как "1",
// и сноска появится внизу страницы.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Вставьте еще текст и отметьте его концевой сноской с пользовательским ссылочным знаком,
// который будет использоваться вместо числа "2" и установит "IsAuto" в значение false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Сноски всегда отображаются внизу текста, на который они ссылаются,
// поэтому этот разрыв страницы не повлияет на сноску.
// С другой стороны, концевые сноски всегда находятся в конце документа.
// так что этот разрыв страницы перенесет концевую сноску на следующую страницу.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
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

* пространство имен [Aspose.Words.Notes](../../aspose.words.notes/)
* сборка [Aspose.Words](../../)
