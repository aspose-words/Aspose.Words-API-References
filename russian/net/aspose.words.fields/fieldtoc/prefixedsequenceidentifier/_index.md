---
title: FieldToc.PrefixedSequenceIdentifier
second_title: Справочник по API Aspose.Words для .NET
description: FieldToc свойство. Получает или задает идентификатор последовательности для которой к номеру страницы записи следует добавить префикс.
type: docs
weight: 120
url: /ru/net/aspose.words.fields/fieldtoc/prefixedsequenceidentifier/
---
## FieldToc.PrefixedSequenceIdentifier property

Получает или задает идентификатор последовательности, для которой к номеру страницы записи следует добавить префикс.

```csharp
public string PrefixedSequenceIdentifier { get; set; }
```

### Примеры

Показывает, как заполнить поле TOC записями с использованием полей SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создавать запись в своей таблице содержания для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, включающий поле SEQ и номер страницы, на которой отображается это поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Поля SEQ отображают счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные счетчики для каждой уникальной именованной последовательности
// идентифицируется свойством SequenceIdentifier поля SEQ.
// Используйте свойство TableOfFiguresLabel, чтобы назвать основную последовательность оглавления.
// Теперь этот TOC будет создавать записи только из полей SEQ, для которых для параметра «SequenceIdentifier» установлено значение «MySequence».
fieldToc.TableOfFiguresLabel = "MySequence";

// Мы можем назвать другую последовательность полей SEQ в свойстве «PrefixedSequenceIdentifier».
 // Поля SEQ из этой последовательности префиксов не будут создавать записи TOC.
// Каждая запись TOC, созданная из поля SEQ основной последовательности, теперь также будет отображать количество, которое
// последовательность префикса в настоящее время включена в поле SEQ основной последовательности, в котором была сделана запись.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Каждая запись оглавления будет отображать счетчик последовательности префикса сразу слева
// номера страницы, на которой отображается поле SEQ основной последовательности.
// Мы можем указать собственный разделитель, который будет стоять между этими двумя числами.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Существует два способа использования полей SEQ для заполнения этого содержания.
// 1 – Вставка поля SEQ, которое принадлежит последовательности префикса TOC:
// Это поле увеличит счетчик последовательностей SEQ для «PrefixSequence» на 1.
// Так как это поле не принадлежит идентифицированной основной последовательности
// по свойству «TableOfFiguresLabel» оглавления, оно не будет отображаться как запись.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 – Вставка поля SEQ, которое принадлежит основной последовательности TOC:
// Это поле SEQ создаст запись в оглавлении.
// Запись оглавления будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно появляется.
// Эта запись также будет отображать счетчик, на котором в данный момент находится последовательность префикса,
// отделено от номера страницы значением свойства SeqenceSeparator оглавления.
// Счетчик «PrefixSequence» равен 1, это поле SEQ основной последовательности находится на странице 2,
// и разделителем является «>», поэтому в записи будет отображаться «1>2».
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Вставьте страницу, увеличьте последовательность префиксов на 2 и вставьте поле SEQ, чтобы впоследствии создать запись оглавления.
// Последовательность префикса теперь равна 2, а поле SEQ основной последовательности находится на странице 3,
// поэтому запись оглавления будет отображать "2>3" при количестве страниц.
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

* class [FieldToc](../)
* пространство имен [Aspose.Words.Fields](../../fieldtoc/)
* сборка [Aspose.Words](../../../)


