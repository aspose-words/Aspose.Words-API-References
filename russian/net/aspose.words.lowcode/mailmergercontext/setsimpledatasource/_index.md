---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words для .NET
description: Повысьте эффективность слияния почты с помощью метода MailMergerContext SetSimpleDataSource, оптимизирующего настройку источника данных для бесперебойного выполнения.
type: docs
weight: 40
url: /ru/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

Устанавливает источник данных, используемый для выполнения простого слияния почты.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## Примечания

Если указаны как источник данных для простого слияния почты, так и источник данных для слияния почты с регионами, то сначала выполняется слияние почты с регионами , а затем выполняется простое слияние почты.

## Примеры

Показывает, как выполнить операцию слияния почты для одной записи с использованием контекста.

```csharp
// Существует несколько способов выполнить операцию слияния почты:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Показывает, как выполнить операцию слияния почты для одной записи из потока с использованием контекста.

```csharp
// Существует несколько способов выполнить операцию слияния почты с использованием документов из потока:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Смотрите также

* class [MailMergerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

Устанавливает источник данных, используемый для выполнения простого слияния почты.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## Примечания

Если указаны как источник данных для простого слияния почты, так и источник данных для слияния почты с регионами, то сначала выполняется слияние почты с регионами , а затем выполняется простое слияние почты.

## Примеры

Показывает, как выполнить операцию слияния почты из DataRow с использованием контекста.

```csharp
// Существует несколько способов выполнить операцию слияния почты из DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataRow);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataRow.docx")
    .Execute();
```

Показывает, как выполнить операцию слияния почты из DataRow, используя документы из потока с использованием контекста.

```csharp
// Существует несколько способов выполнить операцию слияния почты из DataRow, используя документы из потока:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataRow);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataRow.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Смотрите также

* class [MailMergerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

Устанавливает источник данных, используемый для выполнения простого слияния почты.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## Примечания

Если указаны как источник данных для простого слияния почты, так и источник данных для слияния почты с регионами, то сначала выполняется слияние почты с регионами , а затем выполняется простое слияние почты.

## Примеры

Показывает, как выполнить операцию слияния почты из DataTable с использованием контекста.

```csharp
// Существует несколько способов выполнить операцию слияния почты из DataTable:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataTable);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataTable.docx")
    .Execute();
```

Показывает, как выполнить операцию слияния почты из DataTable, используя документы из потока с использованием контекста.

```csharp
// Существует несколько способов выполнить операцию слияния почты из DataTable, используя документы из потока:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Смотрите также

* class [MailMergerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
