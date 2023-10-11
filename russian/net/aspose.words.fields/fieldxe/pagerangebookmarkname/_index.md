---
title: FieldXE.PageRangeBookmarkName
second_title: Справочник по API Aspose.Words для .NET
description: FieldXE свойство. Получает или задает имя закладки которая отмечает диапазон страниц вставленных в качестве номера страницы записи.
type: docs
weight: 60
url: /ru/net/aspose.words.fields/fieldxe/pagerangebookmarkname/
---
## FieldXE.PageRangeBookmarkName property

Получает или задает имя закладки, которая отмечает диапазон страниц, вставленных в качестве номера страницы записи.

```csharp
public string PageRangeBookmarkName { get; set; }
```

### Примеры

Показывает, как указать составные страницы закладки в качестве диапазона страниц для записи поля ИНДЕКС.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте поле INDEX, в котором будет отображаться запись для каждого поля XE, найденного в документе.
// Каждая запись будет отображать значение свойства Text поля XE слева,
// и номер страницы, содержащей поле XE справа.
// Запись INDEX соберет все поля XE с совпадающими значениями в свойстве «Текст».
// в одну запись, а не вводить запись для каждого поля XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Для записей INDEX, отображающих диапазоны страниц, мы можем указать строку-разделитель
// который появится между номером первой страницы и номером последней.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Если поле XE называет закладку, используя свойство PageRangeBookmarkName,
// его запись INDEX покажет диапазон страниц, охватываемых закладкой
// вместо номера страницы, содержащей поле XE.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// Вставляем закладку, которая начинается на странице 3 и заканчивается на странице 5.
// Запись INDEX для поля XE, которое ссылается на эту закладку, отобразит этот диапазон страниц.
// В нашей таблице запись ИНДЕКС будет отображать «Моя запись на страницах с 3 по 5».
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

* class [FieldXE](../)
* пространство имен [Aspose.Words.Fields](../../fieldxe/)
* сборка [Aspose.Words](../../../)


