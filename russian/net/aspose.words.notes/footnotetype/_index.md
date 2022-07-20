---
title: FootnoteType
second_title: Справочник по API Aspose.Words для .NET
description: Указывает является ли это сноской или концевой сноской.
type: docs
weight: 4060
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
| Footnote | `0` | Объект представляет собой сноску. |
| Endnote | `1` | Объект является концевой сноской. |

### Примечания

И сноски, и концевые сноски представлены объектами с помощьюFootnote класс. Использовать[`FootnoteType`](../footnote/footnotetype) различать сноски и концевые сноски.

### Примеры

Показывает, как ссылаться на текст со сноской и концевой сноской.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем некоторый текст и помечаем его сноской со свойством IsAuto, для которого по умолчанию установлено значение «true»,
// поэтому маркер, видимый в основном тексте, будет автоматически пронумерован как «1»,
// и сноска появится внизу страницы.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Вставьте дополнительный текст и отметьте его концевой сноской с пользовательской контрольной меткой,
// который будет использоваться вместо числа "2" и установить для "IsAuto" значение false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Сноски всегда появляются внизу текста, на который они ссылаются,
// поэтому этот разрыв страницы не повлияет на сноску.
// С другой стороны, концевые сноски всегда находятся в конце документа
// чтобы этот разрыв страницы переместил концевую сноску на следующую страницу.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
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

* пространство имен [Aspose.Words.Notes](../../aspose.words.notes)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->