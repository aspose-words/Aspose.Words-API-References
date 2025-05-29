---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.MailMergeCleanupOptions для эффективного управления очисткой слияния почты. Оптимизируйте свои документы, легко контролируя удаление элементов.
type: docs
weight: 4540
url: /ru/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Указывает параметры, определяющие, какие элементы удаляются во время слияния почты.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Указывает значение по умолчанию. |
| RemoveEmptyParagraphs | `1` | Указывает, следует ли удалять из документа абзацы, содержащие поля слияния почты без данных. Если этот параметр установлен, абзацы, содержащие поля слияния начала и конца области, которые в противном случае были бы пустыми , также удаляются. |
| RemoveUnusedRegions | `2` | Указывает, следует ли удалять из документа неиспользуемые области слияния почты. |
| RemoveUnusedFields | `4` | Указывает, следует ли удалять из документа неиспользуемые поля слияния. |
| RemoveContainingFields | `8` | Указывает, следует ли удалять из документа поля, содержащие поля слияния (например, IF), если удаляются вложенные поля слияния. |
| RemoveStaticFields | `10` | Указывает, следует ли удалять статические поля из документа. Статические поля — это поля, результаты которых остаются неизменными при любом изменении документа. Поля, которые не сохраняют свои результаты в document и вычисляются «на лету» (например,FieldListNum , FieldSymbol и т. д.) не считаются статическими. |
| RemoveEmptyTableRows | `20` | Указывает, следует ли удалять из документа пустые строки, содержащие области слияния почты. |
| RemoveEmptyTables | `40` | Указывает, следует ли удалять из таблиц документа, которые содержат области слияния почты, удаленные с помощью либоRemoveUnusedRegions илиRemoveEmptyTableRows вариант. |

## Примеры

Показывает, как удалить всю пустую таблицу во время слияния почты.

```csharp
DataTable tableCustomers = new DataTable("A");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataSet ds = new DataSet();
ds.Tables.Add(tableCustomers);

Document doc = new Document(MyDir + "Mail merge tables.docx");
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

doc.MailMerge.MergeDuplicateRegions = false;
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyTables | MailMergeCleanupOptions.RemoveUnusedRegions;
doc.MailMerge.ExecuteWithRegions(ds.Tables["A"]);

doc.Save(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");

doc = new Document(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");
Assert.AreEqual(1, doc.GetChildNodes(NodeType.Table, true).Count);
```

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

* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../)
