---
title: MailMerger.ExecuteWithRegionsToImages
linktitle: ExecuteWithRegionsToImages
articleTitle: ExecuteWithRegionsToImages
second_title: Aspose.Words для .NET
description: Легко объединяйте данные из DataTable в документы с помощью MailMerger ExecuteWithRegionsToImages, превращая ваш контент в потрясающие изображения.
type: docs
weight: 50
url: /ru/net/aspose.words.lowcode/mailmerger/executewithregionstoimages/
---
## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_3}

Выполняет слияние почты из DataTable в документ с областями слияния почты и отображает результат в виде изображений.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| dataTable | DataTable | Таблица, содержащая данные для вставки в поля слияния. Имена полей нечувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты с регионами из DataTable и сохранить результат в виде изображений.

```csharp
// Существует несколько способов выполнить операцию слияния почты с регионами из DataTable:
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

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_1}

Выполняет слияние почты из DataTable в документ с областями слияния почты и отображает результат в виде изображений.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| dataTable | DataTable | Таблица, содержащая данные для вставки в поля слияния. Имена полей нечувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты с регионами из DataTable, используя документы из потока, и сохранить результат в виде изображений.

```csharp
// Существует несколько способов выполнить операцию слияния почты с регионами из DataTable, используя документы из потока:
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

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages_2}

Выполняет слияние почты из DataSet в документ с областями слияния почты и отображает результат в виде изображений.

```csharp
public static Stream[] ExecuteWithRegionsToImages(string inputFileName, 
    ImageSaveOptions saveOptions, DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| dataSet | DataSet | DataSet, содержащий данные для вставки в поля слияния почты. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты с регионами из DataSet и сохранить результат в виде изображений.

```csharp
// Существует несколько способов выполнить операцию слияния почты с регионами из DataSet:
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

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegionsToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../../mailmergeoptions/)*) {#executewithregionstoimages}

Выполняет слияние почты из DataSet в документ с областями слияния почты и отображает результат в виде изображений.

```csharp
public static Stream[] ExecuteWithRegionsToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataSet dataSet, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| dataSet | DataSet | DataSet, содержащий данные для вставки в поля слияния почты. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты с регионами из DataSet, используя документы из потока, и сохранить результат в виде изображений.

```csharp
// Существует несколько способов выполнить операцию слияния почты с регионами из DataSet, используя документы из потока:
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

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
