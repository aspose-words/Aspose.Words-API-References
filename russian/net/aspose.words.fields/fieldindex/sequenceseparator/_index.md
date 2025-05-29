---
title: FieldIndex.SequenceSeparator
linktitle: SequenceSeparator
articleTitle: SequenceSeparator
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldIndex SequenceSeparator, легко управляйте последовательностями символов для разделения последовательностей и номеров страниц в ваших приложениях.
type: docs
weight: 160
url: /ru/net/aspose.words.fields/fieldindex/sequenceseparator/
---
## FieldIndex.SequenceSeparator property

Возвращает или задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц.

```csharp
public string SequenceSeparator { get; set; }
```

## Примеры

Показывает, как разделить документ на части, объединив поля INDEX и SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Если поля XE имеют одинаковое значение в свойстве "Текст",
// поле ИНДЕКС сгруппирует их в одну запись.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// В свойстве SequenceName назовите последовательность поля SEQ. Каждая запись этого поля INDEX теперь также будет отображать
// номер, на котором находится счетчик последовательности в месте расположения поля XE, создавшего эту запись.
index.SequenceName = "MySequence";

// Установите текст вокруг последовательности и номеров страниц, чтобы объяснить их значение пользователю.
// Запись, созданная с помощью этой конфигурации, будет отображать что-то вроде «MySequence at 1 on page 1» на своем номере страницы.
// PageNumberSeparator и SequenceSeparator не могут быть длиннее 15 символов.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// Поля SEQ отображают счетчик, который увеличивается в каждом поле SEQ.
// Эти поля также поддерживают отдельные подсчеты для каждой уникальной именованной последовательности
// идентифицируется свойством "SequenceIdentifier" поля SEQ.
// Вставьте поле SEQ, которое перемещает последовательность «MySequence» на 1.
// Это поле ничем не отличается от обычного текста документа. Оно не будет отображаться в таблице содержания поля INDEX.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Вставьте поле XE, которое создаст запись в поле INDEX.
// Поскольку "MySequence" имеет значение 1, а это поле XE находится на странице 2, вместе с пользовательскими разделителями, которые мы определили выше,
// запись INDEX этого поля отобразит «Cat» слева и «MySequence at 1 on page 2» справа.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Вставьте разрыв страницы и используйте поля SEQ для перемещения «MySequence» на 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Вставьте поле XE с тем же свойством Text, что и выше.
// Запись INDEX сгруппирует поля XE с соответствующими значениями в свойстве «Текст»
// в одну запись, а не вводить запись для каждого поля XE.
// Поскольку мы находимся на странице 2 с «MySequence» на 3, «, 3 на странице 3» будет добавлено к той же записи INDEX, что и выше.
// Часть номера страницы этой записи INDEX теперь будет отображать «MySequence at 1 on page 2, 3 on page 3».
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Вставьте поле XE с новым и уникальным значением свойства Text.
// Это добавит новую запись с MySequence на 3 на странице 4.
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
