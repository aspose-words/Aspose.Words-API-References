---
title: FieldSeq.ResetNumber
linktitle: ResetNumber
articleTitle: ResetNumber
second_title: Aspose.Words для .NET
description: Управляйте свойством FieldSeq ResetNumber без усилий! Задайте или извлеките целое число для управления порядковыми номерами, гарантируя точную обработку данных.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldseq/resetnumber/
---
## FieldSeq.ResetNumber property

Возвращает или задает целое число для сброса порядкового номера. Возвращает -1, если номер отсутствует.

```csharp
public string ResetNumber { get; set; }
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

### Смотрите также

* class [FieldSeq](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
