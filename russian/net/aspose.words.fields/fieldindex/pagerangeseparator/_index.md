---
title: FieldIndex.PageRangeSeparator
linktitle: PageRangeSeparator
articleTitle: PageRangeSeparator
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageRangeSeparator в FieldIndex. Легко настройте последовательность символов для бесшовного форматирования диапазона страниц и улучшите ясность вашего документа.
type: docs
weight: 130
url: /ru/net/aspose.words.fields/fieldindex/pagerangeseparator/
---
## FieldIndex.PageRangeSeparator property

Возвращает или задает последовательность символов, которая используется для разделения начала и конца диапазона страниц.

```csharp
public string PageRangeSeparator { get; set; }
```

## Примеры

Показывает, как указать охватываемые страницы закладки в качестве диапазона страниц для записи поля ИНДЕКС.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, которое будет отображать запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX соберет все поля XE с соответствующими значениями в свойстве «Текст»
// в одну запись, а не вводить запись для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Для записей INDEX, отображающих диапазоны страниц, мы можем указать строку-разделитель
// который будет отображаться между номером первой страницы и номером последней.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Если поле XE называет закладку, используя свойство PageRangeBookmarkName,
// его запись INDEX покажет диапазон страниц, которые охватывает закладка
// вместо номера страницы, содержащей поле XE.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// Вставьте закладку, которая начинается на странице 3 и заканчивается на странице 5.
// Запись INDEX для поля XE, ссылающегося на эту закладку, отобразит этот диапазон страниц.
// В нашей таблице запись INDEX будет отображать «Моя запись, на страницах с 3 по 5».
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### Смотрите также

* class [FieldIndex](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
