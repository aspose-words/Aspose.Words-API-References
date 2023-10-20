---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words для .NET
description: MailMerge GetFieldNames метод. Возвращает коллекцию имен полей слияния почты доступных в документе на С#.
type: docs
weight: 220
url: /ru/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Возвращает коллекцию имен полей слияния почты, доступных в документе.

```csharp
public string[] GetFieldNames()
```

## Примечания

Возвращает полные имена полей слияния, включая необязательный префикс. Не удаляет повторяющиеся имена полей.

Новый массив строк создается при каждом вызове.

Включает имена полей с «усами», если[`UseNonMergeFields`](../usenonmergefields/) является`истинный`.

## Примеры

Показывает, как получить имена всех полей слияния в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Columns.Add("City");
dataTable.Rows.Add(new object[] { "John", "Doe", "New York" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs", "Washington" });

// Для каждого имени MERGEFIELD в документе убедитесь, что таблица данных содержит столбец
 // с тем же именем, а затем выполнить слияние почты.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
