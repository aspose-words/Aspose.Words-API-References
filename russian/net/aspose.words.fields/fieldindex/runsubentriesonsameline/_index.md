---
title: FieldIndex.RunSubentriesOnSameLine
linktitle: RunSubentriesOnSameLine
articleTitle: RunSubentriesOnSameLine
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldIndex RunSubentriesOnSameLine, позволяющее легко управлять подзаписями, встроенными в основные записи, для оптимизированной организации данных.
type: docs
weight: 140
url: /ru/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Возвращает или задает, следует ли запускать подзаписи в той же строке, что и основная запись.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

## Примеры

Показывает, как работать с подзаписями в поле INDEX.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX соберет все поля XE с соответствующими значениями в свойстве «Текст»
// в одну запись, а не вводить запись для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// Поля XE, имеющие свойство Text, значение которого становится заголовком записи INDEX.
// Если это значение содержит два строковых сегмента, разделенных двоеточием (запись INDEX будет рассматривать разделитель :),
// первый сегмент — заголовок, а второй сегмент станет подзаголовком.
// Поле INDEX сначала группирует записи в алфавитном порядке, затем, если есть несколько полей XE с одинаковыми
// заголовков, поле ИНДЕКС дополнительно подгруппирует их по значениям этих заголовков.
// Может быть несколько слоев подгрупп, в зависимости от того, сколько раз
// Текстовые свойства полей XE сегментируются следующим образом.
// По умолчанию группа записей поля ИНДЕКС создаст новую строку для каждого подзаголовка в этой группе.
// Мы можем установить флаг RunSubentriesOnSameLine в значение true, чтобы сохранить заголовок,
// и каждый подзаголовок для группы на одной строке, что сделает поле ИНДЕКС более компактным.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Вставьте два поля XE, каждое на новой странице, и с одинаковым заголовком «Заголовок 1»,
// который поле INDEX будет использовать для их группировки.
// Если RunSubentriesOnSameLine имеет значение false, то таблица INDEX создаст три строки:
// одна строка для группирующего заголовка «Заголовок 1» и еще по одной строке для каждого подзаголовка.
// Если RunSubentriesOnSameLine имеет значение true, то таблица INDEX создаст однострочную
// запись, которая охватывает заголовок и каждый подзаголовок.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 1";

Assert.AreEqual(" XE  \"Heading 1:Subheading 1\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Heading 1:Subheading 2";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + $"Field.INDEX.XE.Subheading.docx");
```

### Смотрите также

* class [FieldIndex](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
