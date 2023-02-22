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
| dataSource | IMailMergeDataSource | Объект, реализующий настраиваемый интерфейс источника данных для слияния почты. |

### Примечания

Используйте этот метод для заполнения полей слияния в документе значениями from любого источника данных, например списка, хеш-таблицы или объектов. Вам нужно написать собственный класс your , реализующий[`IMailMergeDataSource`](../../imailmergedatasource/) интерфейс.

Вы можете использовать этот метод только тогда, когда[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)ложно, то есть вам не нужна совместимость с языками с письмом справа налево (такими как арабский или иврит).

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
| values | Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно совпадать с количеством элементов в fieldNames. |

### Примечания

Используйте этот метод, чтобы заполнить поля слияния в документе значениями from из массива объектов.

Этот метод объединяет данные только для одной записи. Массив имен полей и массив значений представляют собой данные одной записи.

Этот метод не использует регионы слияния.

Этот метод игнорируетRemoveUnusedRegions вариант.

### Примеры

Показывает, как объединить изображение из URI в качестве данных слияния почты в поле MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELD с тегами «Image:» получат изображение во время слияния почты.
// Строка после двоеточия в теге "Image:" соответствует имени столбца
// в источнике данных, ячейки которого содержат URI файлов изображений.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Создадим источник данных, содержащий URI изображений, которые мы объединим.
// URI может быть веб-URL, указывающим на изображение, или именем файла изображения в локальной файловой системе.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Выполнить слияние для источника данных с одной строкой.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Показывает, как выполнить слияние почты, а затем сохранить документ в браузере клиента.

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
    Throws.TypeOf<ArgumentNullException>()); // Выброшено, потому что HttpResponse имеет значение null в тесте.

// Нам нужно будет закрыть этот ответ вручную, чтобы гарантировать, что мы не добавим лишний контент в документ после сохранения.
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
| table | DataTable | Таблица, содержащая данные для вставки в поля слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, не найденное в документе, оно игнорируется. |

### Примечания

Используйте этот метод для заполнения полей слияния в документе значениями из a . **Таблица данных**.

Все записи из таблицы объединяются в документ.

Вы можете использовать поле NEXT в документе Word, чтобы вызвать **MailMerge** объект для select следующей записи из **Таблица данных** и продолжить слияние. Это можно использовать при создании таких документов, как почтовые ярлыки.

Когда **MailMerge**объект достигает конца основного документа, а в таблице еще больше строк **Таблица данных**, он копирует все содержимое основного документа и добавляет его в конец целевого документа, используя в качестве разделителя разрыв section .

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

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния.
    // 1 — использовать всю таблицу для слияния, чтобы создать один выходной документ слияния для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния почты:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ слияния.
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

Выполняет слияние почты из IDataReader в документ.

```csharp
public void Execute(IDataReader dataReader)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataReader | IDataReader | Источник данных для операции слияния почты. |

### Примечания

Вы можете пройти **SqlDataReader** или же **Оледбдатаридер** объект в метод this в качестве параметра, потому что они оба реализовали **IDataReader** интерфейс.

Обратите внимание, что этот метод не использует области слияния почты, и для нескольких записей документ будет увеличиваться за счет повторения всего документа.

Этот метод игнорируетRemoveUnusedRegions вариант.

### Примеры

Показывает, как выполнить слияние с использованием данных из устройства чтения данных.

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
string connectionString = @"Driver={Microsoft Access Driver (*.mdb)};Dbq=" + DatabaseDir + "Northwind.mdb";
string query = 
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, {fn ROUND(Products.UnitPrice,2)} as UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OdbcConnection connection = new OdbcConnection())
{
    connection.ConnectionString = connectionString;
    connection.Open();

    // Создайте команду SQL, которая будет источником данных для нашего слияния.
    // Имена столбцов таблицы, которые вернет этот оператор SELECT
    // должны соответствовать полям слияния, которые мы разместили выше.
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

    // Это запустит команду и сохранит данные в считывателе.
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

    // Берём данные из ридера и используем их в слиянии.
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Выполняет слияние почты из DataView в документ.

```csharp
public void Execute(DataView dataView)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataView | DataView | Источник данных для операции слияния почты. |

### Примечания

Этот метод полезен, если вы извлекаете данные в **Таблица данных** но тогда нужно применять фильтр или сортировать перед слиянием почты.

Обратите внимание, что этот метод не использует области слияния почты, и для нескольких записей документ будет увеличиваться за счет повторения всего документа.

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

// Создаем таблицу данных, из которой наше слияние будет получать данные.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Мы можем использовать представление данных для изменения данных слияния без внесения изменений в саму таблицу данных.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Наше представление данных сортирует записи в порядке убывания по столбцу «Оценка»
// и отфильтровывает строки со значениями меньше 50 в этом столбце.
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

Выполняет слияние почты из DataRow в документ.

```csharp
public void Execute(DataRow row)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | DataRow | Строка, содержащая данные для вставки в поля слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, не найденное в документе, оно игнорируется. |

### Примечания

Используйте этот метод для заполнения полей слияния в документе значениями из **DataRow**.

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

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния.
    // 1 — использовать всю таблицу для слияния, чтобы создать один выходной документ слияния для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния почты:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ слияния.
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


