---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldSeq BookmarkName для легкого управления навигацией по документу. Установите или извлеките имена закладок для бесшовного ссылания на элементы.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Возвращает или задает имя закладки, которое ссылается на элемент в другом месте документа, а не в текущем местоположении.

```csharp
public string BookmarkName { get; set; }
```

## Примеры

Показывает, как объединить оглавление и поля последовательности.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создать запись в своей таблице содержания для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, содержащий поле SEQ,
// и номер страницы, на которой отображается поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Настройте это поле TOC так, чтобы оно имело свойство SequenceIdentifier со значением «MySequence».
fieldToc.TableOfFiguresLabel = "MySequence";

// Настройте это поле TOC так, чтобы оно выбирало только поля SEQ, находящиеся в пределах закладки
// с именем "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// Поля SEQ отображают счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные подсчеты для каждой уникальной именованной последовательности
// идентифицируется свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, имеющее идентификатор последовательности, соответствующий TOC
// Свойство TableOfFiguresLabel. Это поле не создаст запись в TOC, так как оно находится за пределами
// границы закладки, обозначенные "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Последовательность этого поля SEQ соответствует свойству "TableOfFiguresLabel" оглавления и находится в пределах закладки.
// Абзац, содержащий это поле, будет отображаться в оглавлении как запись.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Последовательность этого поля SEQ не соответствует свойству "TableOfFiguresLabel" оглавления,
// и находится в пределах закладки. Его абзац не будет отображаться в оглавлении как запись.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Последовательность этого поля SEQ соответствует свойству "TableOfFiguresLabel" оглавления и находится в пределах закладки.
// Это поле также ссылается на другую закладку. Содержимое этой закладки появится в записи TOC для этого поля SEQ.
// Само поле SEQ не будет отображать содержимое этой закладки.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Создайте закладку с содержимым, которое будет отображаться в записи оглавления, поскольку указанное выше поле SEQ ссылается на нее.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### Смотрите также

* class [FieldSeq](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
