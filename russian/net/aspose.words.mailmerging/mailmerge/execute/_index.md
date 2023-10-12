---
title: MailMerge.Execute
second_title: Справочник по API Aspose.Words для .NET
description: MailMerge метод. Выполняет слияние почты из пользовательского источника данных.
type: docs
weight: 180
url: /ru/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

Выполняет слияние почты из пользовательского источника данных.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Объект, реализующий пользовательский интерфейс источника данных слияния почты. |

### Примечания

Используйте этот метод, чтобы заполнить поля слияния почты в документе значениями из любого источника данных, такого как список, хэш-таблица или объекты. Вам нужно написать собственный класс your , реализующий[`IMailMergeDataSource`](../../imailmergedatasource/) интерфейс.

Вы можете использовать этот метод только тогда, когда[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) является`ЛОЖЬ`, то есть вам не нужна совместимость с языками с письмом справа налево (например, арабским или ивритом).

Этот метод игнорируетRemoveUnusedRegions вариант.

### Смотрите также

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

Выполняет операцию слияния почты для одной записи.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldNames | String[] | Массив имен полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |
| values | Object[] | Массив значений, которые будут вставлены в поля слияния. Количество элементов в этом массиве должно быть таким же, как количество элементов в*fieldNames*. |

### Примечания

Используйте этот метод для заполнения полей слияния почты в документе значениями из массива объектов.

Этот метод объединяет данные только для одной записи. Массив полей name и массив значений представляют данные одной записи.

Этот метод не использует регионы слияния почты.

Этот метод игнорируетRemoveUnusedRegions вариант.

### Примеры

Показывает, как объединить изображение из URI в качестве данных слияния почты в MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELD с тегами «Image:» получит изображение во время слияния почты.
// Строка после двоеточия в теге "Image:" соответствует имени столбца
// в источнике данных, ячейки которого содержат URI файлов изображений.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Создаем источник данных, содержащий URI изображений, которые мы объединим.
// URI может быть веб-URL, указывающим на изображение, или именем файла изображения в локальной файловой системе.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Выполняем слияние почты для источника данных с одной строкой.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Показывает, как выполнить слияние почты, а затем сохранить документ в клиентском браузере.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Отправляем документ в клиентский браузер.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Выбрасывается, потому что HttpResponse в тесте имеет значение null.

// Нам нужно будет закрыть этот ответ вручную, чтобы гарантировать, что мы не добавим в документ лишний контент после сохранения.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

Выполняет слияние почты из DataTable в документ.

```csharp
public void Execute(DataTable table)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| table | DataTable | Таблица, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |

### Примечания

Используйте этот метод для заполнения полей слияния почты в документе значениями из a . **Таблица данных**.

Все записи из таблицы объединяются в документ.

Вы можете использовать поле NEXT в документе Word, чтобы вызвать[`MailMerge`](../) объект для выбора следующей записи из **Таблица данных** и продолжить объединение. Это можно использовать при создании документов, таких как почтовые этикетки.

Когда[`MailMerge`](../) объект достигает конца основного документа, и в нем еще осталось строк more  **Таблица данных**, он копирует все содержимое основного документа и добавляет его в конец целевого документа, используя разрывsection в качестве разделителя.

Этот метод игнорируетRemoveUnusedRegions вариант.

### Примеры

Показывает, как выполнить слияние почты с данными из DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния почты.
    // 1 — использовать всю таблицу для слияния почты, чтобы создать один выходной документ слияния почты для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 — использовать одну строку таблицы для создания одного выходного документа слияния почты:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ слияния почты.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

Выполняет слияние почты из **Идатаридер** в документ.

```csharp
public void Execute(IDataReader dataReader)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataReader | IDataReader | Источник данных для операции слияния почты. |

### Примечания

Вы можете пройти **SqlDataReader** или **ОлеДбDataReader** объект в метод this в качестве параметра, поскольку они оба реализовали **Идатаридер** интерфейс.

Обратите внимание, что этот метод не использует регионы слияния почты, и для нескольких записей документ the будет увеличиваться, повторяя весь документ.

Этот метод игнорируетRemoveUnusedRegions вариант.

### Примеры

Показывает, как запустить слияние почты, используя данные из устройства чтения данных.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Product:\t");
builder.InsertField(" MERGEFIELD ProductName");
builder.Write("\nSupplier:\t");
builder.InsertField(" MERGEFIELD CompanyName");
builder.Writeln();
builder.InsertField(" MERGEFIELD QuantityPerUnit");
builder.Write(" for $");
builder.InsertField(" MERGEFIELD UnitPrice");

// Создаем строку подключения, указывающую на файл базы данных "Борей"
// в нашей локальной файловой системе открываем соединение и настраиваем SQL-запрос.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Создайте команду SQL, которая будет источником данных для нашего слияния почты.
    // Имена столбцов таблицы, которые вернет этот оператор SELECT
    // должно соответствовать полям слияния, которые мы разместили выше.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {                    
        connection.Open();                 
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Берём данные из считывателя и используем их при слиянии почты.
            doc.MailMerge.Execute(reader);
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }                
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Выполняет слияние почты из **Просмотр данных** в документ.

```csharp
public void Execute(DataView dataView)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataView | DataView | Источник данных для операции слияния почты. |

### Примечания

Этот метод полезен, если вы извлекаете данные в **Таблица данных** но тогда необходимо применить фильтр или сортировку перед слиянием почты.

Обратите внимание, что этот метод не использует регионы слияния почты, и для нескольких записей документ the будет увеличиваться, повторяя весь документ.

Этот метод игнорируетRemoveUnusedRegions вариант.

### Примеры

Показывает, как редактировать данные слияния почты с помощью DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Создайте таблицу данных, из которой наше слияние почты будет получать данные.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Мы можем использовать представление данных, чтобы изменить данные слияния почты, не внося изменений в саму таблицу данных.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Наше представление данных сортирует записи в порядке убывания по столбцу «Оценка».
// и отфильтровывает строки со значениями менее 50 в этом столбце.
// Три из четырех строк соответствуют этим критериям, поэтому выходной документ будет содержать три документа слияния.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

Выполняет слияние почты из **Строка данных** в документ.

```csharp
public void Execute(DataRow row)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | DataRow | Строка, содержащая данные для вставки в поля слияния почты. Имена полей не чувствительны к регистру. Если встречается имя поля, которого нет в документе, оно игнорируется. |

### Примечания

Используйте этот метод, чтобы заполнить поля слияния в документе значениями из **Строка данных**.

Этот метод игнорируетRemoveUnusedRegions вариант.

### Примеры

Показывает, как выполнить слияние почты с данными из DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния почты.
    // 1 — использовать всю таблицу для слияния почты, чтобы создать один выходной документ слияния почты для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 — использовать одну строку таблицы для создания одного выходного документа слияния почты:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ слияния почты.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)


