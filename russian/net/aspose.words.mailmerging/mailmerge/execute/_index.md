---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words для .NET
description: Оптимизируйте процесс рассылки с помощью метода MailMerge Execute, который позволяет легко объединять данные из пользовательских источников для персонализированного общения.
type: docs
weight: 180
url: /ru/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

Выполняет слияние почты из пользовательского источника данных.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Объект, реализующий пользовательский интерфейс источника данных для слияния почты. |

## Примечания

Используйте этот метод для заполнения полей слияния в документе значениями from любого источника данных, например списка, хэш-таблицы или объектов. Вам нужно написать your собственный класс, который реализует[`IMailMergeDataSource`](../../imailmergedatasource/) интерфейс.

Вы можете использовать этот метод только тогда, когда[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) является`ЛОЖЬ`, то есть вам не нужна совместимость с языками с письмом справа налево (например, арабским или ивритом).

Этот метод игнорируетRemoveUnusedRegions вариант.

## Примеры

Показывает, как выполнить слияние почты с источником данных в виде пользовательского объекта.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>
    {
        new Customer("Thomas Hardy", "120 Hanover Sq., London"),
        new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino")
    };

     // Чтобы использовать пользовательский объект в качестве источника данных, он должен реализовывать интерфейс IMailMergeDataSource.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Пример класса «сущность данных» в вашем приложении.
/// </summary>
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
 /// Пользовательский источник данных для слияния почты, который вы реализуете, чтобы разрешить Aspose.Words
/// для слияния данных из объектов Customer в документы Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Когда мы инициализируем источник данных, его позиция должна быть перед первой записью.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяющимися регионами.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words вызывает этот метод, чтобы получить значение для каждого поля данных.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mCustomers[mRecordIndex].FullName;
                return true;
            case "Address":
                fieldValue = mCustomers[mRecordIndex].Address;
                return true;
            default:
                // Возвращаем "false" в движок слияния почты Aspose.Words, чтобы обозначить
                // что мы не смогли найти поле с таким именем.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Стандартная реализация перехода к следующей записи в коллекции.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly List<Customer> mCustomers;
    private int mRecordIndex;
}
```

### Смотрите также

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

Выполняет операцию слияния почты для одной записи.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldNames | String[] | Массив имен полей слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, которое не найдено в документе, оно игнорируется. |
| values | Object[] | Массив значений для вставки в поля слияния. Количество элементов в этом массиве должно быть таким же, как количество элементов в*fieldNames*. |

## Примечания

Используйте этот метод для заполнения полей слияния в документе значениями from массива объектов.

Этот метод объединяет данные только для одной записи. Массив имен полей и массив значений представляют данные одной записи.

Этот метод не использует области слияния почты.

Этот метод игнорируетRemoveUnusedRegions вариант.

## Примеры

Показывает, как объединить изображение из URI в виде данных слияния почты в MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELD с тегами «Image:» получат изображение во время слияния почты.
// Строка после двоеточия в теге "Image:" соответствует имени столбца
// в источнике данных, ячейки которого содержат URI файлов изображений.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Создаем источник данных, содержащий URI изображений, которые мы будем объединять.
// URI может быть веб-URL, указывающим на изображение, или именем файла изображения в локальной файловой системе.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Выполнить слияние почты для источника данных с одной строкой.
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
//Выброшено, потому что HttpResponse имеет значение null в тесте.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Нам нужно будет закрыть этот ответ вручную, чтобы гарантировать, что мы не добавим в документ лишнего содержимого после сохранения.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

Выполняет слияние почты из DataTable в документ.

```csharp
public void Execute(DataTable table)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| table | DataTable | Таблица, содержащая данные для вставки в поля слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, отсутствующее в документе, оно игнорируется. |

## Примечания

Используйте этот метод для заполнения полей слияния в документе значениями из a **Таблица данных**.

Все записи из таблицы объединяются в документ.

Вы можете использовать поле NEXT в документе Word, чтобы вызвать[`MailMerge`](../) объект для select следующей записи из**Таблица данных** и продолжить объединение. Это можно использовать при создании таких документов, как почтовые этикетки.

Когда[`MailMerge`](../) объект достигает конца основного документа, а в нем все еще есть more строк**Таблица данных**он копирует все содержимое основного документа и добавляет его в конец целевого документа, используя разрыв section в качестве разделителя.

Этот метод игнорируетRemoveUnusedRegions вариант.

## Примеры

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
    // 1 - Использовать всю таблицу для слияния почты, чтобы создать один выходной документ слияния почты для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ для слияния почты.
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
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

Выполняет слияние почты из**IDataReader** в документ.

```csharp
public void Execute(IDataReader dataReader)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataReader | IDataReader | Источник данных для операции слияния почты. |

## Примечания

Вы можете пройти**SqlDataReader** или**OleDbDataReader**объект в метод this как параметр, поскольку они оба реализовали**IDataReader** интерфейс.

Обратите внимание, что этот метод не использует области слияния почты, и для нескольких записей документ the будет увеличиваться за счет повторения всего документа.

Этот метод игнорируетRemoveUnusedRegions вариант.

## Примеры

Показывает, как выполнить слияние почты, используя данные из программы чтения данных.

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

// Создаем строку подключения, указывающую на файл базы данных «Northwind»
// в нашей локальной файловой системе открываем соединение и настраиваем SQL-запрос.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Создаем команду SQL, которая будет источником данных для нашего слияния.
    // Имена столбцов таблицы, которые вернет этот оператор SELECT
    // должны будут соответствовать полям слияния, которые мы разместили выше.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {
        connection.Open();
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // Берем данные от ридера и используем их при слиянии писем.
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
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

Выполняет слияние почты из**Просмотр данных** в документ.

```csharp
public void Execute(DataView dataView)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataView | DataView | Источник данных для операции слияния почты. |

## Примечания

Этот метод полезен, если вы извлекаете данные в**Таблица данных** но then необходимо применить фильтр или сортировку перед слиянием почты.

Обратите внимание, что этот метод не использует области слияния почты, и для нескольких записей документ the будет увеличиваться за счет повторения всего документа.

Этот метод игнорируетRemoveUnusedRegions вариант.

## Примеры

Показывает, как редактировать данные слияния с помощью DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Создаем таблицу данных, из которой будут браться данные для слияния писем.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Мы можем использовать представление данных для изменения данных слияния почты, не внося изменений в саму таблицу данных.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Наше представление данных сортирует записи в порядке убывания по столбцу «Оценка»
// и отфильтровывает строки со значениями менее 50 в этом столбце.
// Три из четырех строк соответствуют этим критериям, поэтому выходной документ будет содержать три объединенных документа.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

Выполняет слияние почты из**DataRow** в документ.

```csharp
public void Execute(DataRow row)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | DataRow | Строка, содержащая данные для вставки в поля слияния. Имена полей не чувствительны к регистру. Если встречается имя поля, отсутствующее в документе, оно игнорируется. |

## Примечания

Используйте этот метод для заполнения полей слияния в документе значениями из**DataRow**.

Этот метод игнорируетRemoveUnusedRegions вариант.

## Примеры

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
    // 1 - Использовать всю таблицу для слияния почты, чтобы создать один выходной документ слияния почты для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ для слияния почты.
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
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
