---
title: SequenceIdentifier
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает имя присвоенное серии элементов которые должны быть пронумерованы.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Получает или задает имя, присвоенное серии элементов, которые должны быть пронумерованы.

```csharp
public string SequenceIdentifier { get; set; }
```

### Примеры

Показывает создание нумерации с использованием полей SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создать запись в своем содержании для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, содержащий поле SEQ, и номер страницы, на которой появляется это поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// В полях SEQ отображается счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные счетчики для каждой уникальной именованной последовательности
// определяется свойством "SequenceIdentifier" поля SEQ.
// Используйте свойство «TableOfFiguresLabel», чтобы назвать основную последовательность для TOC.
// Теперь этот оглавление будет создавать только записи из полей SEQ с их «SequenceIdentifier», установленным на «MySequence».
fieldToc.TableOfFiguresLabel = "MySequence";

// Мы можем назвать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
 // Поля SEQ из этой последовательности префиксов не будут создавать записи TOC.
// Каждая запись TOC, созданная из поля SEQ основной последовательности, теперь также будет отображать количество, которое
// последовательность префикса в настоящее время включена в поле SEQ первичной последовательности, которое сделало запись.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Каждая запись TOC будет отображать счетчик последовательностей префиксов сразу слева
// номера страницы, на которой появляется поле SEQ основной последовательности.
// Мы можем указать собственный разделитель, который будет отображаться между этими двумя числами.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Существует два способа использования полей SEQ для заполнения этого оглавления.
// 1 - Вставка поля SEQ, принадлежащего префиксной последовательности TOC:
// Это поле увеличит счетчик последовательности SEQ для «PrefixSequence» на 1.
// Так как это поле не принадлежит идентифицированной основной последовательности
// по свойству "TableOfFiguresLabel" оглавления оно не будет отображаться как запись.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Вставка поля SEQ, принадлежащего основной последовательности TOC:
// Это поле SEQ создаст запись в оглавлении.
// Запись TOC будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно появляется.
// Эта запись также будет отображать счетчик, на котором в данный момент находится последовательность префиксов,
// отделяется от номера страницы значением свойства SeqenceSeparator оглавления.
// Счетчик «PrefixSequence» равен 1, это поле SEQ основной последовательности находится на странице 2,
// и разделитель ">", поэтому запись будет отображать "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Вставьте страницу, продвиньте последовательность префиксов на 2 и вставьте поле SEQ, чтобы впоследствии создать запись оглавления.
// Последовательность префикса теперь равна 2, а поле SEQ основной последовательности находится на странице 3,
// таким образом, запись оглавления будет отображать "2>3" на количестве страниц.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

Показывает, как заполнить поле TOC записями, используя поля SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создать запись в своем содержании для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, содержащий поле SEQ, и номер страницы, на которой появляется это поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// В полях SEQ отображается счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные счетчики для каждой уникальной именованной последовательности
// определяется свойством "SequenceIdentifier" поля SEQ.
// Используйте свойство «TableOfFiguresLabel», чтобы назвать основную последовательность для TOC.
// Теперь этот оглавление будет создавать только записи из полей SEQ с их «SequenceIdentifier», установленным на «MySequence».
fieldToc.TableOfFiguresLabel = "MySequence";

// Мы можем назвать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
 // Поля SEQ из этой последовательности префиксов не будут создавать записи TOC.
// Каждая запись TOC, созданная из поля SEQ основной последовательности, теперь также будет отображать количество, которое
// последовательность префикса в настоящее время включена в поле SEQ первичной последовательности, которое сделало запись.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Каждая запись TOC будет отображать счетчик последовательностей префиксов сразу слева
// номера страницы, на которой появляется поле SEQ основной последовательности.
// Мы можем указать собственный разделитель, который будет отображаться между этими двумя числами.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Существует два способа использования полей SEQ для заполнения этого оглавления.
// 1 - Вставка поля SEQ, принадлежащего префиксной последовательности TOC:
// Это поле увеличит счетчик последовательности SEQ для «PrefixSequence» на 1.
// Так как это поле не принадлежит идентифицированной основной последовательности
// по свойству "TableOfFiguresLabel" оглавления оно не будет отображаться как запись.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Вставка поля SEQ, принадлежащего основной последовательности TOC:
// Это поле SEQ создаст запись в оглавлении.
// Запись TOC будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно появляется.
// Эта запись также будет отображать счетчик, на котором в данный момент находится последовательность префиксов,
// отделяется от номера страницы значением свойства SeqenceSeparator оглавления.
// Счетчик «PrefixSequence» равен 1, это поле SEQ основной последовательности находится на странице 2,
// и разделитель ">", поэтому запись будет отображать "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Вставьте страницу, продвиньте последовательность префиксов на 2 и вставьте поле SEQ, чтобы впоследствии создать запись оглавления.
// Последовательность префикса теперь равна 2, а поле SEQ основной последовательности находится на странице 3,
// таким образом, запись оглавления будет отображать "2>3" на количестве страниц.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Смотрите также

* class [FieldSeq](../../fieldseq)
* пространство имен [Aspose.Words.Fields](../../fieldseq)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
