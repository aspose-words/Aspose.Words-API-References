---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: Aspose.Words for .NET
description: 使用 MailMerger ExecuteToImages 方法轻松地对单个记录执行邮件合并并将结果转换为高质量图像。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

对单个记录执行邮件合并操作并将结果呈现为图像。

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| fieldValues | Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何对单个记录进行邮件合并操作并将结果保存为图像。

```csharp
// 有几种方法可以进行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

对单个记录执行邮件合并操作并将结果呈现为图像。

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| fieldValues | Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何对流中的单个记录执行邮件合并操作并将结果保存为图像。

```csharp
// 有几种方法可以使用流中的文档进行邮件合并操作：
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);

    MailMergeOptions mailMergeOptions = new MailMergeOptions();
    mailMergeOptions.TrimWhitespaces = true;
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

执行从 DataRow 到文档的邮件合并并将结果呈现为图像。

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| dataRow | DataRow | 包含要插入邮件合并字段的数据的行。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何从 DataRow 执行邮件合并操作并将结果保存为图像。

```csharp
// 有几种方法可以从 DataRow 执行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

执行从 DataRow 到文档的邮件合并并将结果呈现为图像。

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| dataRow | DataRow | 包含要插入邮件合并字段的数据的行。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何使用流中的文档从 DataRow 执行邮件合并操作并将结果保存为图像。

```csharp
// 有几种方法可以使用流中的文档从 DataRow 执行邮件合并操作：
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

执行从 DataRow 到文档的邮件合并并将结果呈现为图像。

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何从 DataTable 执行邮件合并操作并将结果保存为图像。

```csharp
// 有几种方法可以从 DataTable 执行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

执行从 DataRow 到文档的邮件合并并将结果呈现为图像。

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| saveOptions | ImageSaveOptions | 输出的保存选项。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 例子

展示如何使用流中的文档从 DataTable 执行邮件合并操作并保存为图像。

```csharp
// 有几种方法可以使用流中的文档从 DataTable 执行邮件合并操作并将结果保存为图像：
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    Stream[] images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable);
    images = MailMerger.ExecuteToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
