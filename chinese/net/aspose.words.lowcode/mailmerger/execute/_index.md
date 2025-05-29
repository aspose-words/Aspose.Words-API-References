---
title: MailMerger.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words for .NET
description: 使用 MailMerger Execute 方法简化您的工作流程，轻松合并单个记录的数据以提高效率和准确性。
type: docs
weight: 20
url: /zh/net/aspose.words.lowcode/mailmerger/execute/
---
## Execute(*string, string, string[], object[]*) {#execute_14}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(string inputFileName, string outputFileName, string[] fieldNames, 
    object[] fieldValues)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| fieldValues | Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何对单个记录进行邮件合并操作。

```csharp
// 有几种方法可以进行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### 也可以看看

* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_8}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 输出的保存格式。 |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| fieldValues | Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何对单个记录进行邮件合并操作。

```csharp
// 有几种方法可以进行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_11}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 输出的保存选项。 |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| fieldValues | Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_2}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| outputStream | Stream | 输出文件流。 |
| saveFormat | SaveFormat | 输出的保存格式。 |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| fieldValues | Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何对流中的单个记录执行邮件合并操作。

```csharp
// 有几种方法可以使用流中的文档进行邮件合并操作：
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, fieldNames, fieldValues);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        MailMergeOptions mailMergeOptions = new MailMergeOptions();
        mailMergeOptions.TrimWhitespaces = true;
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
    }
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#execute_5}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| outputStream | Stream | 输出文件流。 |
| saveOptions | SaveOptions | 输出的保存选项。 |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| fieldValues | Object[] | 要插入合并字段的值数组。此数组中的元素数量必须与 fieldNames 中的元素数量相同。 |
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

## Execute(*string, string, DataRow*) {#execute_12}

执行从 DataRow 到文档的邮件合并。

```csharp
public static void Execute(string inputFileName, string outputFileName, DataRow dataRow)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| dataRow | DataRow | 包含要插入邮件合并字段的数据的行。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何从 DataRow 执行邮件合并操作。

```csharp
// 有几种方法可以从 DataRow 执行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.1.docx", dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.2.docx", SaveFormat.Docx, dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.3.docx", SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_6}

执行从 DataRow 到文档的邮件合并。

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 输出的保存格式。 |
| dataRow | DataRow | 包含要插入邮件合并字段的数据的行。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何从 DataRow 执行邮件合并操作。

```csharp
// 有几种方法可以从 DataRow 执行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.1.docx", dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.2.docx", SaveFormat.Docx, dataRow);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataRow.3.docx", SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_9}

执行从 DataRow 到文档的邮件合并。

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 输出的保存选项。 |
| dataRow | DataRow | 包含要插入邮件合并字段的数据的行。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| outputStream | Stream | 输出文件流。 |
| saveFormat | SaveFormat | 输出的保存格式。 |
| dataRow | DataRow | 包含要插入邮件合并字段的数据的行。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
| mailMergeOptions | MailMergeOptions | 邮件合并选项。 |

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何使用流中的文档从 DataRow 执行邮件合并操作。

```csharp
// 有几种方法可以使用流中的文档从 DataRow 执行邮件合并操作：
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamDataRow.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataRow);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeStreamDataRow.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataRow, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_3}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入文件流。 |
| outputStream | Stream | 输出文件流。 |
| saveOptions | SaveOptions | 输出的保存选项。 |
| dataRow | DataRow | 包含要插入邮件合并字段的数据的行。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段名称。 |
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

## Execute(*string, string, DataTable*) {#execute_13}

将 DataTable 中的邮件合并到文档中。

```csharp
public static void Execute(string inputFileName, string outputFileName, DataTable dataTable)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| dataTable | DataTable | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到文档中不存在的字段名称，则会忽略该字段。 |

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何从 DataTable 执行邮件合并操作。

```csharp
// 有几种方法可以从 DataTable 执行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_7}

执行从 DataRow 到文档的邮件合并。

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

展示如何从 DataTable 执行邮件合并操作。

```csharp
// 有几种方法可以从 DataTable 执行邮件合并操作：
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMergeDataTable.3.docx", SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_10}

执行从 DataRow 到文档的邮件合并。

```csharp
public static void Execute(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

## Execute(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_1}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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

展示如何使用流中的文档从 DataTable 执行邮件合并操作。

```csharp
// 有几种方法可以使用流中的文档从 DataTable 执行邮件合并操作：
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeDataTable.1.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataTable);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeDataTable.2.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Execute(streamIn, streamOut, SaveFormat.Docx, dataTable, new MailMergeOptions() { TrimWhitespaces = true });
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#execute_4}

对单个记录执行邮件合并操作。

```csharp
public static void Execute(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
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
