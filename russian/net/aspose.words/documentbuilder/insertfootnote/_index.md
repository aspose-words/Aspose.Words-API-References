---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words для .NET
description: DocumentBuilder InsertFootnote метод. Вставляет в документ сноску или концевую сноску на С#.
type: docs
weight: 330
url: /ru/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Вставляет в документ сноску или концевую сноску.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteType | FootnoteType | Указывает, вставлять ли сноску или концевую сноску. |
| footnoteText | String | Указывает текст сноски. |

### Возвращаемое значение

Возвращает только что созданный объект сноски.

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

### Смотрите также

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Вставляет в документ сноску или концевую сноску.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteType | FootnoteType | Указывает, вставлять ли сноску или концевую сноску. |
| footnoteText | String | Указывает текст сноски. |
| referenceMark | String | Указывает пользовательский ссылочный знак сноски. |

### Возвращаемое значение

Возвращает только что созданный объект сноски.

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

### Смотрите также

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
