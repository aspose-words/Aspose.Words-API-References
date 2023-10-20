---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words для .NET
description: Aspose.Words.Notes.FootnoteType перечисление. Указывает является ли это сноской или концевой сноской на С#.
type: docs
weight: 4300
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
| Footnote | `0` | Объект является сноской. |
| Endnote | `1` | Объект является сноской. |

## Примечания

И сноски, и концевые сноски представлены объектами с помощьюFootnote класс. Использовать[`FootnoteType`](../footnote/footnotetype/) чтобы различать сноски и концевые сноски.

## Примеры

Показывает, как ссылаться на текст с помощью сноски и концевой сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем текст и отмечаем его сноской со свойством IsAuto, установленным по умолчанию в значение «true»,
// поэтому маркер, видимый в основном тексте, будет автоматически пронумерован как "1",
// и сноска появится внизу страницы.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Вставляем дополнительный текст и отмечаем его концевой сноской с помощью пользовательского ссылочного знака,
// который будет использоваться вместо числа «2» и установит для «IsAuto» значение false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Сноски всегда появляются внизу текста, на который они ссылаются,
// поэтому разрыв страницы не повлияет на сноску.
// С другой стороны, концевые сноски всегда находятся в конце документа
// так что этот разрыв страницы переместит сноску вниз на следующую страницу.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

Показывает, как вставлять и настраивать сноски.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем текст и ссылаемся на него с помощью сноски. В этой сноске будет помещена небольшая надстрочная ссылка.
// отмечаем после текста, на который он ссылается, и создаем запись под основным текстом внизу страницы.
// Эта запись будет содержать знак ссылки на сноску и текст ссылки,
// который мы передадим методу компоновщика документов "InsertFootnote".
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Если для этого свойства установлено значение «true», то ссылочный знак нашей сноски
// будет его индексом среди всех сносок раздела.
// Это первая сноска, поэтому контрольной отметкой будет «1».
Assert.True(footnote.IsAuto);

 // Мы можем переместить конструктор документа внутрь сноски, чтобы редактировать ссылочный текст.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Мы можем установить собственный ссылочный знак, который будет использоваться в сноске вместо порядкового номера.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Закладка с флагом «IsAuto», установленным в true, все равно будет показывать свой реальный индекс
// даже если предыдущие закладки отображают пользовательские метки, метка этой закладки будет «3».
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Notes](../../aspose.words.notes/)
* сборка [Aspose.Words](../../)
