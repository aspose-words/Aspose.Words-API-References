---
title: MailMergerContext.SetRegionsDataSource
linktitle: SetRegionsDataSource
articleTitle: SetRegionsDataSource
second_title: Aspose.Words for .NET
description: 使用 MailMergerContext SetRegionsDataSource 方法无缝设置区域数据源，从而提高邮件合并效率。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/mailmergercontext/setregionsdatasource/
---
## SetRegionsDataSource(*DataTable*) {#setregionsdatasource_1}

设置用于执行区域邮件合并的数据源。

```csharp
public void SetRegionsDataSource(DataTable dataTable)
```

## 评论

如果同时指定了简单邮件合并数据源和带区域邮件合并数据源，则首先执行 带区域邮件合并，然后执行简单邮件合并。

## 例子

展示如何使用上下文从 DataTable 进行区域邮件合并操作。

```csharp
// 有几种方法可以通过 DataTable 进行区域邮件合并操作：
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetRegionsDataSource(dataTable);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextWithRegionsDataTable.docx")
    .Execute();
```

展示如何使用来自流的文档通过上下文从 DataTable 执行带有区域操作的邮件合并。

```csharp
// 有几种方法可以使用来自流的文档从 DataTable 进行区域邮件合并操作：
DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetRegionsDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamWithRegionsDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
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

## SetRegionsDataSource(*DataSet*) {#setregionsdatasource}

设置用于执行区域邮件合并的数据源。

```csharp
public void SetRegionsDataSource(DataSet dataSet)
```

## 评论

如果同时指定了简单邮件合并数据源和带区域邮件合并数据源，则首先执行 带区域邮件合并，然后执行简单邮件合并。

## 例子

展示如何使用上下文从数据集进行区域邮件合并操作。

```csharp
// 有几种方法可以通过 DataSet 进行区域邮件合并操作：
string doc = MyDir + "Mail merge with regions data set.docx";

DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetRegionsDataSource(dataSet);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextWithRegionsDataTable.docx")
    .Execute();
```

展示如何使用来自流的文档通过上下文从 DataSet 执行带有区域操作的邮件合并。

```csharp
// 有几种方法可以使用来自流的文档从 DataSet 进行区域邮件合并操作：
DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetRegionsDataSource(dataSet);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamWithRegionsDataSet.docx", FileMode.Create, FileAccess.ReadWrite))
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
