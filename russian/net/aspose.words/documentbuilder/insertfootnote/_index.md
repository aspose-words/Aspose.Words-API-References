---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words для .NET
description: Улучшайте свои документы без особых усилий с помощью метода InsertFootnote в DocumentBuilder — легко добавляйте сноски или концевые сноски для большей ясности и профессионализма.
type: docs
weight: 340
url: /ru/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Вставляет сноску или концевую сноску в документ.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteType | FootnoteType | Указывает, следует ли вставлять сноску или концевую сноску. |
| footnoteText | String | Указывает текст сноски. |

### Возвращаемое значение

Возвращает объект сноски, который был только что создан.

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

### Смотрите также

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Вставляет сноску или концевую сноску в документ.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteType | FootnoteType | Указывает, следует ли вставлять сноску или концевую сноску. |
| footnoteText | String | Указывает текст сноски. |
| referenceMark | String | Задает пользовательский ссылочный знак сноски. |

### Возвращаемое значение

Возвращает объект сноски, который был только что создан.

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

### Смотрите также

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
