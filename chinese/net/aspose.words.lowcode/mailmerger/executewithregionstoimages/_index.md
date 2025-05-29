---
title: MailMerger.ExecuteWithRegionsToImages
linktitle: ExecuteWithRegionsToImages
articleTitle: ExecuteWithRegionsToImages
second_title: Aspose.Words for .NET
description: 使用 MailMerger ExecuteWithRegionsToImages 轻松地将 DataTable 中的数据合并到文档中，将您的内容转换为令人惊叹的图像。
type: docs
weight: 50
url: /zh/net/aspose.words.lowcode/mailmerger/executewithregionstoimages/
---
## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_3}

使用邮件合并区域将 DataTable 中的邮件合并到文档中，并将结果呈现为图像。

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何从 DataTable 进行区域邮件合并操作并将结果保存为图像。

```csharp
// 有几种方法可以通过 DataTable 进行区域邮件合并操作：
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

Stream[] images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_1}

使用邮件合并区域将 DataTable 中的邮件合并到文档中，并将结果呈现为图像。

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何使用流中的文档从 DataTable 执行区域操作的邮件合并并将结果保存为图像。

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
    Stream[] images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_2}

使用邮件合并区域将 DataSet 中的邮件合并到文档中，并将结果呈现为图像。

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| dataSet | DataSet | 包含要插入邮件合并字段的数据的数据集。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何从数据集进行区域操作邮件合并并将结果保存为图像。

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

Stream[] images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataSet);
images = MailMerger.ExecuteWithRegionsToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages}

使用邮件合并区域将 DataSet 中的邮件合并到文档中，并将结果呈现为图像。

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| dataSet | DataSet | 包含要插入邮件合并字段的数据的数据集。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何使用流中的文档从数据集执行区域邮件合并操作并将结果保存为图像。

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
    Stream[] images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataSet);
    images = MailMerger.ExecuteWithRegionsToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataSet, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
