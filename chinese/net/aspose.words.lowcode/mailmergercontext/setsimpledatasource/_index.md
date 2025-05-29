---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words for .NET
description: 使用 MailMergerContext SetSimpleDataSource 方法提高邮件合并效率，简化数据源设置以实现无缝执行。
type: docs
weight: 40
url: /zh/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

设置用于执行简单邮件合并的数据源。

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## 评论

如果同时指定了简单邮件合并数据源和带区域邮件合并数据源，则首先执行 带区域邮件合并，然后执行简单邮件合并。

## 例子

展示如何使用上下文对单个记录执行邮件合并操作。

```csharp
// 有几种方法可以进行邮件合并操作：
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

展示如何使用上下文对流中的单个记录执行邮件合并操作。

```csharp
// 有几种方法可以使用流中的文档进行邮件合并操作：
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

### 也可以看看

* class [MailMergerContext](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

设置用于执行简单邮件合并的数据源。

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## 评论

如果同时指定了简单邮件合并数据源和带区域邮件合并数据源，则首先执行 带区域邮件合并，然后执行简单邮件合并。

## 例子

展示如何使用上下文从 DataRow 执行邮件合并操作。

```csharp
// 有几种方法可以从 DataRow 执行邮件合并操作：
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

展示如何使用来自流的文档通过上下文从 DataRow 执行邮件合并操作。

```csharp
// 有几种方法可以使用流中的文档从 DataRow 执行邮件合并操作：
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

### 也可以看看

* class [MailMergerContext](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

设置用于执行简单邮件合并的数据源。

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## 评论

如果同时指定了简单邮件合并数据源和带区域邮件合并数据源，则首先执行 带区域邮件合并，然后执行简单邮件合并。

## 例子

展示如何使用上下文从 DataTable 执行邮件合并操作。

```csharp
// 有几种方法可以从 DataTable 执行邮件合并操作：
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

展示如何使用来自流的文档通过上下文从 DataTable 执行邮件合并操作。

```csharp
// 有几种方法可以使用流中的文档从 DataTable 执行邮件合并操作：
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

### 也可以看看

* class [MailMergerContext](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
