---
title: MailMerge.CleanupOptions
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words для .NET
description: Оптимизируйте процесс слияния писем с помощью свойства CleanupOptions — легко управляйте тем, какие элементы следует удалить, для обеспечения бесперебойного и эффективного процесса.
type: docs
weight: 10
url: /ru/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

Возвращает или задает набор флагов, которые определяют, какие элементы следует удалить во время слияния почты.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

## Примеры

Показывает, как удалить пустые абзацы, которые могут возникнуть при слиянии почты, из выходного документа слияния.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.AreEqual(
        "John Doe\r" +
        "Jane Doe", doc.GetText().Trim());
else
    Assert.AreEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.GetText().Trim());
```

Показывает, как автоматически удалять поля MERGEFIELD, которые не используются во время слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем документ с MERGEFIELD для трех столбцов исходной таблицы данных слияния,
// а затем создадим таблицу только с двумя столбцами, имена которых соответствуют нашим MERGEFIELD.
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

// Наш третий MERGEFIELD ссылается на столбец «Город», которого нет в нашем источнике данных.
// Слияние почты оставит такие поля нетронутыми в том состоянии, в котором они были до слияния.
// Установка свойства "CleanupOptions" в значение "RemoveUnusedFields" удалит все MERGEFIELD
// которые не используются во время слияния почты для очистки документов слияния.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Смотрите также

* enum [MailMergeCleanupOptions](../../mailmergecleanupoptions/)
* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
