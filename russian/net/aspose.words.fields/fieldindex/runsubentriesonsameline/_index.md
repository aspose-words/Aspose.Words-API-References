---
title: FieldIndex.RunSubentriesOnSameLine
second_title: Справочник по API Aspose.Words для .NET
description: FieldIndex свойство. Получает или задает запускать ли подзаписи в той же строке что и основная запись.
type: docs
weight: 140
url: /ru/net/aspose.words.fields/fieldindex/runsubentriesonsameline/
---
## FieldIndex.RunSubentriesOnSameLine property

Получает или задает, запускать ли подзаписи в той же строке, что и основная запись.

```csharp
public bool RunSubentriesOnSameLine { get; set; }
```

### Примеры

Показывает, как работать с подзаписями в поле ИНДЕКС.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, в котором будет отображаться запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX соберет все поля XE с совпадающими значениями в свойстве «Текст».
// в одну запись, а не вводить запись для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.PageNumberSeparator = ", see page ";
index.Heading = "A";

// Поля XE, имеющие свойство Text, значение которого становится заголовком записи INDEX.
// Если это значение содержит два сегмента строки, разделенных двоеточием (запись INDEX будет обрабатывать :) разделитель,
// первый сегмент является заголовком, а второй сегмент станет подзаголовком.
// Поле ИНДЕКС сначала группирует записи в алфавитном порядке, затем, если имеется несколько полей XE с одинаковыми
// заголовки, поле ИНДЕКС далее группирует их по значениям этих заголовков.
// Может быть несколько слоев подгруппы, в зависимости от того, сколько раз
// Текстовые свойства полей XE сегментируются следующим образом.
// По умолчанию группа ввода поля ИНДЕКС создаст новую строку для каждого подзаголовка в этой группе.
// Мы можем установить для флага RunSubentriesOnSameLine значение true, чтобы сохранить заголовок,
// и вместо этого каждый подзаголовок группы в одной строке, что сделает поле ИНДЕКС более компактным.
index.RunSubentriesOnSameLine = runSubentriesOnTheSameLine;

if (runSubentriesOnTheSameLine)
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A \\r", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX  \\e \", see page \" \\h A", index.GetFieldCode());

// Вставляем два поля XE, каждое на новой странице, с одинаковым заголовком «Заголовок 1»,
// который поле ИНДЕКС будет использовать для их группировки.
// Если RunSubentriesOnSameLine имеет значение false, то таблица INDEX создаст три строки:
// одна строка для группирующего заголовка «Заголовок 1» и еще по одной строке для каждого подзаголовка.
// Если RunSubentriesOnSameLine имеет значение true, то таблица INDEX создаст однострочную
// запись, которая включает заголовок и каждый подзаголовок.
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
* пространство имен [Aspose.Words.Fields](../../fieldindex/)
* сборка [Aspose.Words](../../../)


