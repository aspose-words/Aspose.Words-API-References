---
title: Enum MailMergeCleanupOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.MailMerging.MailMergeCleanupOptions перечисление. Указывает параметры определяющие какие элементы удаляются во время слияния почты.
type: docs
weight: 3850
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
| RemoveEmptyParagraphs | `1` | Указывает, следует ли удалять из документа абзацы, содержащие поля слияния почты без данных. Если этот параметр установлен, абзацы, содержащие поля слияния начала и конца региона, которые в противном случае являются пустыми , также удаляются. |
| RemoveUnusedRegions | `2` | Указывает, следует ли удалять из документа неиспользуемые области слияния почты. |
| RemoveUnusedFields | `4` | Указывает, следует ли удалять из документа неиспользуемые поля слияния. |
| RemoveContainingFields | `8` | Указывает, следует ли удалять поля, содержащие поля слияния (например, IF), из документа , если удалены вложенные поля слияния. |
| RemoveStaticFields | `10` | Указывает, следует ли удалять статические поля из документа. Статические поля — это поля, результаты которых остаются неизменными при любом изменении документа. Поля, которые не сохраняют результаты в document и вычисляются «на лету» (например,FieldListNum , FieldSymbol и т. д.) не считаются статическими. |
| RemoveEmptyTableRows | `20` | Указывает, следует ли удалять из документа пустые строки, содержащие области слияния почты. |

### Примеры

Показывает, как удалить пустые абзацы, которые может создать слияние почты, из выходного документа слияния.

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

Показывает, как автоматически удалять поля MERGEFIELD, которые остаются неиспользованными во время слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создаем документ с MERGEFIELD для трех столбцов таблицы источника данных слияния почты,
// а затем создадим таблицу только с двумя столбцами, имена которых соответствуют нашим полям MERGEFIELD.
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
// Слияние почты оставит такие поля нетронутыми в их состоянии до слияния.
// Установка для свойства «CleanupOptions» значения «RemoveUnusedFields» приведет к удалению всех полей MERGEFIELD.
// которые остаются неиспользованными во время слияния почты для очистки документов слияния.
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


