---
title: MailMerger.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words for .NET
description: 使用 MailMerger 的 ExecuteWithRegions 方法简化文档创建。使用可自定义的区域，轻松将 DataTable 合并到文档中。
type: docs
weight: 40
url: /zh/net/aspose.words.lowcode/mailmerger/executewithregions/
---
## ExecuteWithRegions(*string, string, DataTable*) {#executewithregions_9}

使用邮件合并区域将 DataTable 中的邮件合并到文档中。

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    DataTable dataTable)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| dataTable | DataTable | 邮件合并操作的数据源。该表必须设置其 TableName 属性。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何从 DataTable 进行区域邮件合并操作。

```csharp
// 有几种方法可以通过 DataTable 进行区域邮件合并操作：
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_5}

使用邮件合并区域将 DataTable 中的邮件合并到文档中。

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 输出的保存格式。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何从 DataTable 进行区域邮件合并操作。

```csharp
// 有几种方法可以通过 DataTable 进行区域邮件合并操作：
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_7}

使用邮件合并区域将 DataTable 中的邮件合并到文档中。

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 输出的保存选项。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_1}

对单个记录执行邮件合并操作。

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| outputStream | Stream | 输出文件流。 |
| saveFormat | SaveFormat | 输出的保存格式。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何使用流中的文档通过 DataTable 进行区域邮件合并操作。

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
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataTable);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_3}

对单个记录执行邮件合并操作。

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| outputStream | Stream | 输出文件流。 |
| saveOptions | SaveOptions | 输出的保存选项。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, DataSet*) {#executewithregions_8}

使用邮件合并区域执行从数据集到文档的邮件合并。

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, DataSet dataSet)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| dataSet | DataSet | 包含要插入邮件合并字段的数据的数据集。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何从数据集进行区域邮件合并操作。

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

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.1.docx", dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.2.docx", SaveFormat.Docx, dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_4}

使用邮件合并区域将 DataSet 中的邮件合并到文档中。

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 输出的保存格式。 |
| dataSet | DataSet | 包含要插入邮件合并字段的数据的数据集。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何从数据集进行区域邮件合并操作。

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

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.1.docx", dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.2.docx", SaveFormat.Docx, dataSet);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_6}

使用邮件合并区域将 DataSet 中的邮件合并到文档中。

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 输出的保存选项。 |
| dataSet | DataSet | 包含要插入邮件合并字段的数据的数据集。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions}

使用邮件合并区域将 DataSet 中的邮件合并到文档中。

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| outputStream | Stream | 输出文件流。 |
| saveFormat | SaveFormat | 输出的保存格式。 |
| dataSet | DataSet | 包含要插入邮件合并字段的数据的数据集。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何使用来自流的文档从数据集执行带有区域操作的邮件合并。

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
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataSet);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamWithRegionsDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, dataSet, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregions_2}

使用邮件合并区域将 DataSet 中的邮件合并到文档中。

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| outputStream | Stream | 输出文件流。 |
| saveOptions | SaveOptions | 输出的保存选项。 |
| dataSet | DataSet | 包含要插入邮件合并字段的数据的数据集。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
