---
title: MailMerger.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words for .NET
description: Streamline your document creation with MailMerger's ExecuteWithRegions method. Effortlessly merge DataTables into documents using customizable regions.
type: docs
weight: 20
url: /net/aspose.words.lowcode/mailmerger/executewithregions/
---
## ExecuteWithRegions(*string, string, DataTable*) {#executewithregions_13}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| dataTable | DataTable | Data source for the mail merge operation. The table must have its TableName property set. |

## Examples

Shows how to do mail merge with regions operation from a DataTable.

```csharp
// There is a several ways to do mail merge with regions operation from a DataTable:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataTable);
```

### See Also

* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataTable*) {#executewithregions_9}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The output's save format. |
| dataTable | DataTable | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

## Examples

Shows how to do mail merge with regions operation from a DataTable.

```csharp
// There is a several ways to do mail merge with regions operation from a DataTable:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataTable);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [MailMergeOptions](../../mailmergeoptions/), DataTable*) {#executewithregions_7}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, MailMergeOptions mailMergeOptions, DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The output's save format. |
| mailMergeOptions | MailMergeOptions | Mail merge options. |
| dataTable | DataTable | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

## Examples

Shows how to do mail merge with regions operation from a DataTable.

```csharp
// There is a several ways to do mail merge with regions operation from a DataTable:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.1.docx", dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.2.docx", SaveFormat.Docx, dataTable);
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataTable.3.docx", SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataTable);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [MailMergeOptions](../../mailmergeoptions/), DataTable*) {#executewithregions_11}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, MailMergeOptions mailMergeOptions, DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveOptions | SaveOptions | The output's save options. |
| mailMergeOptions | MailMergeOptions | Mail merge options. |
| dataTable | DataTable | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataTable*) {#executewithregions_3}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| outputStream | Stream | The output file stream. |
| saveFormat | SaveFormat | The output's save format. |
| dataTable | DataTable | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

## Examples

Shows how to do mail merge with regions operation from a DataTable using documents from the stream.

```csharp
// There is a several ways to do mail merge with regions operation from a DataTable using documents from the stream:
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
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataTable);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), [MailMergeOptions](../../mailmergeoptions/), DataTable*) {#executewithregions_1}

Performs a mail merge operation for a single record.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, MailMergeOptions mailMergeOptions, DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| outputStream | Stream | The output file stream. |
| saveFormat | SaveFormat | The output's save format. |
| mailMergeOptions | MailMergeOptions | Mail merge options. |
| dataTable | DataTable | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

## Examples

Shows how to do mail merge with regions operation from a DataTable using documents from the stream.

```csharp
// There is a several ways to do mail merge with regions operation from a DataTable using documents from the stream:
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
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataTable);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [MailMergeOptions](../../mailmergeoptions/), DataTable*) {#executewithregions_5}

Performs a mail merge operation for a single record.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, MailMergeOptions mailMergeOptions, DataTable dataTable)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| outputStream | Stream | The output file stream. |
| saveOptions | SaveOptions | The output's save options. |
| mailMergeOptions | MailMergeOptions | Mail merge options. |
| dataTable | DataTable | Table that contains data to be inserted into mail merge fields. Field names are not case sensitive. If a field name that is not found in the document is encountered, it is ignored. |

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, DataSet*) {#executewithregions_12}

Performs mail merge from a DataSet into a document with mail merge regions.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| dataSet | DataSet | DataSet that contains data to be inserted into mail merge fields. |

## Examples

Shows how to do mail merge with regions operation from a DataSet.

```csharp
// There is a several ways to do mail merge with regions operation from a DataSet:
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
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataSet);
```

### See Also

* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), DataSet*) {#executewithregions_8}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The output's save format. |
| dataSet | DataSet | DataSet that contains data to be inserted into mail merge fields. |

## Examples

Shows how to do mail merge with regions operation from a DataSet.

```csharp
// There is a several ways to do mail merge with regions operation from a DataSet:
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
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataSet);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [MailMergeOptions](../../mailmergeoptions/), DataSet*) {#executewithregions_6}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveFormat saveFormat, MailMergeOptions mailMergeOptions, DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The output's save format. |
| mailMergeOptions | MailMergeOptions | Mail merge options. |
| dataSet | DataSet | DataSet that contains data to be inserted into mail merge fields. |

## Examples

Shows how to do mail merge with regions operation from a DataSet.

```csharp
// There is a several ways to do mail merge with regions operation from a DataSet:
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
MailMerger.ExecuteWithRegions(doc, ArtifactsDir + "LowCode.MailMergeWithRegionsDataSet.3.docx", SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataSet);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [MailMergeOptions](../../mailmergeoptions/), DataSet*) {#executewithregions_10}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, MailMergeOptions mailMergeOptions, DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputFileName | String | The input file name. |
| outputFileName | String | The output file name. |
| saveOptions | SaveOptions | The output's save options. |
| mailMergeOptions | MailMergeOptions | Mail merge options. |
| dataSet | DataSet | DataSet that contains data to be inserted into mail merge fields. |

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), DataSet*) {#executewithregions_2}

Performs mail merge from a DataTable into the document with mail merge regions.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| outputStream | Stream | The output file stream. |
| saveFormat | SaveFormat | The output's save format. |
| dataSet | DataSet | DataSet that contains data to be inserted into mail merge fields. |

## Examples

Shows how to do mail merge with regions operation from a DataSet using documents from the stream.

```csharp
// There is a several ways to do mail merge with regions operation from a DataSet using documents from the stream:
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
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataSet);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), [MailMergeOptions](../../mailmergeoptions/), DataSet*) {#executewithregions}

Performs a mail merge operation for a single record.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat, MailMergeOptions mailMergeOptions, DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| outputStream | Stream | The output file stream. |
| saveFormat | SaveFormat | The output's save format. |
| mailMergeOptions | MailMergeOptions | Mail merge options. |
| dataSet | DataSet | DataSet that contains data to be inserted into mail merge fields. |

## Examples

Shows how to do mail merge with regions operation from a DataSet using documents from the stream.

```csharp
// There is a several ways to do mail merge with regions operation from a DataSet using documents from the stream:
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
        MailMerger.ExecuteWithRegions(streamIn, streamOut, SaveFormat.Docx, new MailMergeOptions() { TrimWhitespaces = true }, dataSet);
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## ExecuteWithRegions(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [MailMergeOptions](../../mailmergeoptions/), DataSet*) {#executewithregions_4}

Performs a mail merge operation for a single record.

```csharp
public static void ExecuteWithRegions(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions, MailMergeOptions mailMergeOptions, DataSet dataSet)
```

| Parameter | Type | Description |
| --- | --- | --- |
| inputStream | Stream | The input file stream. |
| outputStream | Stream | The output file stream. |
| saveOptions | SaveOptions | The output's save options. |
| mailMergeOptions | MailMergeOptions | Mail merge options. |
| dataSet | DataSet | DataSet that contains data to be inserted into mail merge fields. |

### See Also

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
