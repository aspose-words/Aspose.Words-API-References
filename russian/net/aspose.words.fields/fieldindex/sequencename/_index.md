---
title: FieldIndex.SequenceName
linktitle: SequenceName
articleTitle: SequenceName
second_title: Aspose.Words для .NET
description: FieldIndex SequenceName свойство. Получает или задает имя последовательности номер которой включен в номер страницы на С#.
type: docs
weight: 150
url: /ru/net/aspose.words.fields/fieldindex/sequencename/
---
## FieldIndex.SequenceName property

Получает или задает имя последовательности, номер которой включен в номер страницы.

```csharp
public string SequenceName { get; set; }
```

## Примеры

Показывает, как разделить документ на части, объединив поля INDEX и SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, в котором будет отображаться запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве «Текст»,
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// В свойстве SequenceName укажите последовательность полей SEQ. Каждая запись в этом поле ИНДЕКС теперь также будет отображать
// число, в котором находится счетчик последовательности в том месте поля XE, которое создало эту запись.
index.SequenceName = "MySequence";

// Установите текст вокруг последовательности и номеров страниц, чтобы объяснить их значение пользователю.
// Запись, созданная с этой конфигурацией, будет отображать что-то вроде «MySequence at 1 на странице 1» по номеру страницы.
// PageNumberSeparator и SequenceSeparator не могут быть длиннее 15 символов.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// Поля SEQ отображают счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные счетчики для каждой уникальной именованной последовательности
// идентифицируется свойством SequenceIdentifier поля SEQ.
// Вставляем поле SEQ, которое перемещает последовательность «MySequence» на 1.
// Это поле ничем не отличается от обычного текста документа. Оно не появится в таблице содержания поля INDEX.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Вставляем поле XE, которое создаст запись в поле INDEX.
// Поскольку «MySequence» имеет значение 1, а это поле XE находится на странице 2 вместе с пользовательскими разделителями, которые мы определили выше,
// запись INDEX этого поля будет отображать «Cat» слева и «MySequence at 1 на странице 2» справа.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Вставьте разрыв страницы и используйте поля SEQ, чтобы переместить «MySequence» на 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Вставляем поле XE с тем же свойством Text, что и выше.
// Запись INDEX сгруппирует поля XE с совпадающими значениями в свойстве «Текст».
// в одну запись, а не вводить запись для каждого поля XE.
// Поскольку мы находимся на странице 2 с «MySequence» в позиции 3, «, 3 на странице 3» будет добавлено к той же записи INDEX, что и выше.
// Часть номера страницы этой записи INDEX теперь будет отображать «MySequence at 1 на странице 2, 3 на странице 3».
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Вставляем поле XE с новым уникальным значением свойства Text.
// Это добавит новую запись с MySequence в позиции 3 на странице 4.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Смотрите также

* class [FieldIndex](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
