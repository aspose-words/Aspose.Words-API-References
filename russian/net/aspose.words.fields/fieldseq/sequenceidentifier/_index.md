---
title: FieldSeq.SequenceIdentifier
linktitle: SequenceIdentifier
articleTitle: SequenceIdentifier
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldSeq SequenceIdentifier, позволяющее легко управлять именами серий элементов и настраивать их для эффективной нумерации и организации.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Возвращает или задает имя, назначенное серии элементов, которые должны быть пронумерованы.

```csharp
public string SequenceIdentifier { get; set; }
```

## Примеры

Демонстрирует создание нумерации с использованием полей SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поля SEQ отображают счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные подсчеты для каждой уникальной именованной последовательности
// идентифицируется свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, которое будет отображать текущее значение счетчика "MySequence",
// после использования свойства "ResetNumber" для установки его на 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Отображаем следующий номер в этой последовательности с другим полем SEQ.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Вставьте заголовок уровня 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Вставьте еще одно поле SEQ из той же последовательности и настройте его для сброса счетчика в каждом заголовке на 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Заголовок выше является заголовком уровня 1, поэтому счетчик для этой последовательности сбрасывается до 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Переходим к следующему числу этой последовательности.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

Показывает, как заполнить поле TOC записями с использованием полей SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Поле TOC может создать запись в своей таблице содержания для каждого поля SEQ, найденного в документе.
// Каждая запись содержит абзац, включающий поле SEQ, и номер страницы, на которой находится это поле.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Поля SEQ отображают счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные подсчеты для каждой уникальной именованной последовательности
// идентифицируется свойством "SequenceIdentifier" поля SEQ.
// Используйте свойство "TableOfFiguresLabel" для наименования основной последовательности для TOC.
// Теперь этот TOC будет создавать записи только из полей SEQ, у которых «SequenceIdentifier» установлен на «MySequence».
fieldToc.TableOfFiguresLabel = "MySequence";

// Мы можем назвать другую последовательность полей SEQ в свойстве "PrefixedSequenceIdentifier".
 // Поля SEQ из этой префиксной последовательности не будут создавать записи TOC.
// Каждая запись TOC, созданная из поля SEQ основной последовательности, теперь также будет отображать количество,
// последовательность префикса в настоящее время находится в поле первичной последовательности SEQ, в котором сделана запись.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Каждая запись TOC будет отображать количество префиксов последовательности сразу слева
// номера страницы, на которой отображается поле основной последовательности SEQ.
// Мы можем указать пользовательский разделитель, который будет отображаться между этими двумя числами.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Существует два способа использования полей SEQ для заполнения этого оглавления.
// 1 - Вставка поля SEQ, принадлежащего префиксной последовательности TOC:
// Это поле увеличит количество последовательностей SEQ для "PrefixSequence" на 1.
// Поскольку это поле не принадлежит к основной последовательности, идентифицированной
// свойством "TableOfFiguresLabel" оглавления, оно не будет отображаться как запись.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Вставка поля SEQ, принадлежащего основной последовательности TOC:
// Это поле SEQ создаст запись в оглавлении.
// Запись TOC будет содержать абзац, в котором находится поле SEQ, и номер страницы, на которой оно появляется.
// Эта запись также отобразит текущее количество префиксной последовательности,
// отделен от номера страницы значением свойства SeqenceSeparator оглавления.
// Счетчик "PrefixSequence" равен 1, это основное поле последовательности SEQ находится на странице 2,
// и разделитель — «>», поэтому запись будет отображать «1>2».
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Вставьте страницу, увеличьте последовательность префиксов на 2 и вставьте поле SEQ, чтобы впоследствии создать запись TOC.
// Последовательность префикса теперь находится на 2, а поле основной последовательности SEQ находится на странице 3,
// поэтому запись TOC будет отображать «2>3» на своем количестве страниц.
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

* class [FieldSeq](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
