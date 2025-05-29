---
title: MailMerger.ExecuteToImages
linktitle: ExecuteToImages
articleTitle: ExecuteToImages
second_title: Aspose.Words для .NET
description: С легкостью выполняйте слияние писем для отдельных записей и преобразуйте результаты в высококачественные изображения с помощью метода MailMerger ExecuteToImages.
type: docs
weight: 30
url: /ru/net/aspose.words.lowcode/mailmerger/executetoimages/
---
## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_5}

Выполняет операцию слияния почты для одной записи и отображает результат в виде изображений.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| fieldNames | String[] | Массив имен полей слияния. Имена полей нечувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| fieldValues | Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно быть таким же, как и количество элементов в fieldNames. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты для одной записи и сохранить результат в виде изображения.

```csharp
// Существует несколько способов выполнить операцию слияния почты:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), fieldNames, fieldValues, mailMergeOptions);
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_2}

Выполняет операцию слияния почты для одной записи и отображает результат в виде изображений.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string[] fieldNames, object[] fieldValues, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| fieldNames | String[] | Массив имен полей слияния. Имена полей нечувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| fieldValues | Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно быть таким же, как и количество элементов в fieldNames. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты для одной записи из потока и сохранить результат в виде изображений.

```csharp
// Существует несколько способов выполнить операцию слияния почты с использованием документов из потока:
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

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_3}

Выполняет слияние почты из DataRow в документ и отображает результат в изображениях.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| dataRow | DataRow | Строка, содержащая данные для вставки в поля слияния. Имена полей нечувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты из DataRow и сохранить результат в виде изображений.

```csharp
// Существует несколько способов выполнить операцию слияния почты из DataRow:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataRow, new MailMergeOptions() { TrimWhitespaces = true });
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages}

Выполняет слияние почты из DataRow в документ и отображает результат в изображениях.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataRow dataRow, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| dataRow | DataRow | Строка, содержащая данные для вставки в поля слияния. Имена полей нечувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты из DataRow, используя документы из потока, и сохранить результат в виде изображений.

```csharp
// Существует несколько способов выполнить операцию слияния почты из DataRow, используя документы из потока:
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

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ExecuteToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_4}

Выполняет слияние почты из DataRow в документ и отображает результат в изображениях.

```csharp
public static Stream[] ExecuteToImages(string inputFileName, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFileName | String | Имя входного файла. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| dataTable | DataTable | Таблица, содержащая данные для вставки в поля слияния. Имена полей нечувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты из DataTable и сохранить результат в виде изображений.

```csharp
// Существует несколько способов выполнить операцию слияния почты из DataTable:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

Stream[] images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable);
images = MailMerger.ExecuteToImages(doc, new ImageSaveOptions(SaveFormat.Png), dataTable, new MailMergeOptions() { TrimWhitespaces = true });
```

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## ExecuteToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../../mailmergeoptions/)*) {#executetoimages_1}

Выполняет слияние почты из DataRow в документ и отображает результат в изображениях.

```csharp
public static Stream[] ExecuteToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    DataTable dataTable, MailMergeOptions mailMergeOptions = null)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | Stream | Входной файловый поток. |
| saveOptions | ImageSaveOptions | Параметры сохранения выходных данных. |
| dataTable | DataTable | Таблица, содержащая данные для вставки в поля слияния. Имена полей нечувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| mailMergeOptions | MailMergeOptions | Параметры слияния почты. |

## Примеры

Показывает, как выполнить операцию слияния почты из DataTable, используя документы из потока и сохраняя их в изображениях.

```csharp
// Существует несколько способов выполнить операцию слияния почты из DataTable, используя документы из потока, и сохранить результат в изображения:
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

### Смотрите также

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMerger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
