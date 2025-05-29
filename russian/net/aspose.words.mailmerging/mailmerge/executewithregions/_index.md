---
title: MailMerge.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words для .NET
description: Оптимизируйте создание документов с помощью метода MailMerge ExecuteWithRegions, обеспечивающего эффективное объединение писем из пользовательских источников данных и регионов.
type: docs
weight: 200
url: /ru/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#executewithregions}

Выполняет слияние почты из пользовательского источника данных с областями слияния почты.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Объект, реализующий пользовательский интерфейс источника данных для слияния почты. |

## Примечания

Используйте этот метод для заполнения полей слияния в документе значениями from любого пользовательского источника данных, такого как XML-файл или коллекции бизнес-объектов. Вам нужно написать your собственный класс, который реализует[`IMailMergeDataSource`](../../imailmergedatasource/) интерфейс.

Вы можете использовать этот метод только тогда, когда[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) является`ЛОЖЬ`, то есть вам не нужна совместимость с языками с письмом справа налево (например, арабским или ивритом).

## Примеры

Показывает, как использовать области слияния почты для выполнения вложенного слияния почты.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Обычно MERGEFIELD содержат имя столбца источника данных слияния почты.
    // Вместо этого мы можем использовать префиксы «TableStart:» и «TableEnd:» для начала/конца области слияния почты.
    // Каждый регион будет принадлежать таблице с именем, соответствующим строке сразу после двоеточия префикса.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Эти поля MERGEFIELD находятся внутри области слияния таблицы «Клиенты».
    // При выполнении слияния почты это поле будет получать данные из строк в источнике данных с именем «Клиенты».
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Создайте вторую область слияния почты внутри внешней области для источника данных с именем «Заказы».
    // Записи данных «Заказы» имеют связь «многие к одному» с источником данных «Клиенты».
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Создать связанные данные с именами, которые соответствуют именам наших регионов слияния.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Для слияния почты из вашего источника данных мы должны обернуть его в объект, реализующий интерфейс IMailMergeDataSource.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
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
        Orders = new List<Order>();
    }

    public string FullName { get; set; }
    public string Address { get; set; }
    public List<Order> Orders { get; set; }
}

/// <summary>
/// Пример типизированной коллекции, содержащей ваши объекты «данных».
/// </summary>
public class CustomerList : ArrayList
{
    public new Customer this[int index]
    {
        get { return (Customer) base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Пример дочернего класса «сущности данных» в вашем приложении.
/// </summary>
public class Order
{
    public Order(string oName, int oQuantity)
    {
        Name = oName;
        Quantity = oQuantity;
    }

    public string Name { get; set; }
    public int Quantity { get; set; }
}

/// <summary>
 /// Пользовательский источник данных для слияния почты, который вы реализуете, чтобы разрешить Aspose.Words
/// для слияния данных из объектов Customer в документы Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
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
        get { return "Customers"; }
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
            case "Order":
                fieldValue = mCustomers[mRecordIndex].Orders;
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
        switch (tableName)
        {
            // Получить дочерний источник данных, имя которого совпадает с областью слияния почты, использующей его столбцы.
            case "Orders":
                return new OrderMailMergeDataSource(mCustomers[mRecordIndex].Orders);
            default:
                return null;
        }
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly CustomerList mCustomers;
    private int mRecordIndex;
}

public class OrderMailMergeDataSource : IMailMergeDataSource
{
    public OrderMailMergeDataSource(List<Order> orders)
    {
        mOrders = orders;

        // Когда мы инициализируем источник данных, его позиция должна быть перед первой записью.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяющимися регионами.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words вызывает этот метод, чтобы получить значение для каждого поля данных.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "Name":
                fieldValue = mOrders[mRecordIndex].Name;
                return true;
            case "Quantity":
                fieldValue = mOrders[mRecordIndex].Quantity;
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

    /// <summary>
    /// Возвращает null, поскольку у нас нет дочерних элементов для этого типа объектов.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mOrders.Count); }
    }

    private readonly List<Order> mOrders;
    private int mRecordIndex;
}
```

### Смотрите также

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(*[IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)*) {#executewithregions_1}

Выполняет слияние почты из пользовательского источника данных с областями слияния почты.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Объект, реализующий пользовательский корневой интерфейс источника данных слияния почты. |

## Примечания

Используйте этот метод для заполнения полей слияния в документе значениями from любого пользовательского источника данных, такого как XML-файл или коллекции бизнес-объектов. Вам необходимо написать собственные классы , которые реализуют[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) и[`IMailMergeDataSource`](../../imailmergedatasource/) интерфейсы.

Вы можете использовать этот метод только тогда, когда[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) является`ЛОЖЬ`, то есть вам не нужна совместимость с языками с письмом справа налево (например, арабским или ивритом).

## Примеры

Выполняет слияние почты из пользовательского источника данных с основными и подробными данными.

```csharp
public void CustomDataSourceRoot()
{
    // Создайте документ с двумя регионами слияния с именами «Вашингтон» и «Сиэтл».
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Создаем два источника данных для слияния почты.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Регистрируем наши источники данных по имени в корне источника данных.
    // Если мы собираемся использовать этот корень источника данных в слиянии почты с регионами,
    // зарегистрированное имя каждого источника должно совпадать с именем существующего региона слияния в исходном документе слияния.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Поскольку у нас есть последовательные регионы слияния почты, нам обычно приходится выполнять два слияния почты.
    // Однако один источник слияния почты с корнем данных может заполнять несколько регионов
    // если корень содержит таблицы с соответствующими именами/именами столбцов.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Создать документ, содержащий последовательные области слияния почты с именами, назначенными входным массивом,
/// для таблицы данных сотрудников.
/// </summary>
private static Document CreateSourceDocumentWithMailMergeRegions(string[] regions)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    foreach (string s in regions)
    {
        builder.Writeln("\n" + s + " branch: ");
        builder.InsertField(" MERGEFIELD TableStart:" + s);
        builder.InsertField(" MERGEFIELD FullName");
        builder.Write(", ");
        builder.InsertField(" MERGEFIELD Department");
        builder.InsertField(" MERGEFIELD TableEnd:" + s);
    }

    return doc;
}

/// <summary>
/// Пример класса «сущность данных» в вашем приложении.
/// </summary>
private class Employee
{
    public Employee(string aFullName, string aDepartment)
    {
        FullName = aFullName;
        Department = aDepartment;
    }

    public string FullName { get; }
    public string Department { get; }
}

/// <summary>
/// Пример типизированной коллекции, содержащей ваши объекты «данных».
/// </summary>
private class EmployeeList : ArrayList
{
    public new Employee this[int index]
    {
        get { return (Employee)base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Корневой источник данных, который можно передать непосредственно в слияние почты, которое может регистрировать и содержать множество дочерних источников данных.
/// Все эти источники должны реализовывать IMailMergeDataSource, а также быть зарегистрированными и различаться по имени
/// что соответствует области слияния почты, которая будет считывать соответствующие данные.
/// </summary>
private class DataSourceRoot : IMailMergeDataSourceRoot
{
    public IMailMergeDataSource GetDataSource(string tableName)
    {
        EmployeeListMailMergeSource source = mSources[tableName];
        source.Reset();
        return mSources[tableName];
    }

    public void RegisterSource(string sourceName, EmployeeListMailMergeSource source)
    {
        mSources.Add(sourceName, source);
    }

    private readonly Dictionary<string, EmployeeListMailMergeSource> mSources = new Dictionary<string, EmployeeListMailMergeSource>();
}

/// <summary>
/// Пользовательский источник данных для слияния почты.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
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

    private bool IsEof
    {
        get { return (mRecordIndex >= mEmployees.Count); }
    }

    public void Reset()
    {
        mRecordIndex = -1;
    }

    /// <summary>
    /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяющимися регионами.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words вызывает этот метод, чтобы получить значение для каждого поля данных.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mEmployees[mRecordIndex].FullName;
                return true;
            case "Department":
                fieldValue = mEmployees[mRecordIndex].Department;
                return true;
            default:
                // Возвращаем "false" в движок слияния почты Aspose.Words, чтобы обозначить
                // что мы не смогли найти поле с таким именем.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Дочерние источники данных предназначены для вложенных почтовых рассылок.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Смотрите также

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataSet*) {#executewithregions_2}

Выполняет слияние почты из**Набор данных** в документ с областями слияния почты.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSet | DataSet | **Набор данных** содержащий данные для вставки в поля слияния почты. |

## Примечания

Используйте этот метод для выполнения слияния почты из одной или нескольких таблиц в повторяющиеся области слияния mail в документе. Области слияния почты внутри документа будут динамически расти для размещения записей в соответствующих таблицах.

Каждый стол в**Набор данных** должно быть имя.

Документ должен иметь области слияния почты, определенные с именами, которые ссылаются на tables в**Набор данных**.

Чтобы указать область слияния в документе, вам необходимо вставить два поля слияния , чтобы обозначить начало и конец области слияния.

Все содержимое документа, включенное в область слияния почты, будет автоматически повторяться для каждой записи в**Таблица данных**.

Чтобы отметить начало области слияния почты, вставьте MERGEFIELD с именем TableStart:MyTable, , где MyTable соответствует одному из имен таблиц в вашем**Набор данных**.

Чтобы обозначить конец области слияния почты, вставьте еще один MERGEFIELD с именем TableEnd:MyTable.

Чтобы вставить MERGEFIELD в Word, используйте команду Вставка/Поле и выберите MergeField, затем введите имя поля x000d.

The**TableStart** и**TableEnd** поля должны находиться в одном и том же разделе документа.

Если используется внутри таблицы,**TableStart** и**TableEnd** должны находиться в одной строке таблицы.

Области слияния в документе должны быть правильно сформированы (всегда должна быть пара совпадающих **TableStart** и**TableEnd** объединить поля с одинаковым именем таблицы).

## Примеры

Показывает, как выполнить вложенное слияние почты с двумя областями слияния и двумя таблицами данных.

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Обычно MERGEFIELD содержат имя столбца источника данных слияния почты.
    // Вместо этого мы можем использовать префиксы «TableStart:» и «TableEnd:» для начала/конца области слияния почты.
    // Каждый регион будет принадлежать таблице с именем, соответствующим строке сразу после двоеточия префикса.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Это поле MERGEFIELD находится внутри области слияния таблицы «Клиенты».
    // При выполнении слияния почты это поле будет получать данные из строк в источнике данных с именем «Клиенты».
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // Создаем заголовки столбцов для таблицы, которая будет содержать значения из второй внутренней области.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // Создайте вторую область слияния почты внутри внешней области для таблицы с именем «Заказы».
    // Таблица «Заказы» имеет связь «многие к одному» с таблицей «Клиенты» по столбцу «CustomerID».
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Завершите внутреннюю область, а затем завершите внешнюю область. Открытие и закрытие области слияния почты должны
    // происходят в одной строке таблицы.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Создаем набор данных, содержащий две таблицы с требуемыми именами и связями.
    // Каждый документ слияния для каждой строки таблицы «Клиенты» внешней области слияния выполнит свое слияние в таблице «Заказы».
    // Каждый объединенный документ будет отображать все строки последней таблицы, значения столбца «CustomerID» которых соответствуют текущей строке таблицы «Customers».
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Создает набор данных, содержащий две таблицы данных с именами «Клиенты» и «Заказы» с отношением «один ко многим» в столбце «CustomerID».
/// </summary>
private static DataSet CreateDataSet()
{
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

    return dataSet;
}
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataTable*) {#executewithregions_3}

Выполняет слияние почты из**Таблица данных** в документ с областями слияния почты.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataTable | DataTable | Источник данных для операции слияния почты. Таблица must имеет свойTableName набор свойств. |

## Примечания

Документ должен иметь область слияния почты, определенную с именем, соответствующим TableName.

Если в документе определены другие области слияния почты, они остаются нетронутыми. Это позволяет выполнять несколько операций слияния почты.

## Примеры

Демонстрирует, как форматировать ячейки во время слияния почты.

```csharp
public void AlternatingRows()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");
}

/// <summary>
/// Форматирует строки таблицы по мере слияния почты, чередуя два цвета в четных/нечетных строках.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Вызывается, когда слияние почты объединяет данные в MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Это верно, если мы находимся в первом столбце, что означает, что мы перешли на новую строку.
        if (args.FieldName == "CompanyName")
        {
            Color rowColor = IsOdd(mRowIdx) ? Color.FromArgb(213, 227, 235) : Color.FromArgb(242, 242, 242);

            for (int colIdx = 0; colIdx < 4; colIdx++)
            {
                mBuilder.MoveToCell(0, mRowIdx, colIdx, 0);
                mBuilder.CellFormat.Shading.BackgroundPatternColor = rowColor;
            }

            mRowIdx++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Ничего не делать.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Функция, необходимая для автопортирования Visual Basic, которая возвращает четность переданного числа.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Создает источник данных для слияния почты.
/// </summary>
private static DataTable GetSuppliersDataTable()
{
    DataTable dataTable = new DataTable("Suppliers");
    dataTable.Columns.Add("CompanyName");
    dataTable.Columns.Add("ContactName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Company " + i;
        datarow[1] = "Contact " + i;
    }

    return dataTable;
}
```

Показывает, как использовать регионы для выполнения двух отдельных слияний в одном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы хотим выполнить два последовательных слияния почты для одного документа, взяв данные из двух таблиц
// связаны друг с другом каким-либо образом, мы можем разделить слияния по регионам.
// Обычно MERGEFIELD содержат имя столбца источника данных слияния почты.
// Вместо этого мы можем использовать префиксы «TableStart:» и «TableEnd:» для начала/конца области слияния почты.
// Каждый регион будет принадлежать таблице с именем, соответствующим строке сразу после двоеточия префикса.
// Эти регионы являются отдельными для несвязанных данных, тогда как для иерархических данных они могут быть вложенными.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Оба MERGEFIELD ссылаются на одно и то же имя столбца, но значения для каждого будут взяты из разных таблиц данных.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Создаем две несвязанные таблицы данных.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Нам нужно будет запустить одно слияние почты на таблицу. Первое слияние почты заполнит MERGEFIELDs
// в диапазоне «Города», оставив поля диапазона «Фрукты» незаполненными.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Выполняем второе слияние для таблицы «Fruit», используя представление данных
// для сортировки строк в порядке возрастания по столбцу «Имя» перед объединением.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataView*) {#executewithregions_4}

Выполняет слияние почты из**Просмотр данных** в документ с областями слияния почты.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataView | DataView | Источник данных для операции слияния почты. Исходная таблица table **Просмотр данных** должен иметь свой**ИмяТаблицы** набор свойств. |

## Примечания

Этот метод полезен, если вы извлекаете данные в**Таблица данных** но then необходимо применить фильтр или сортировку перед слиянием почты.

Документ должен иметь область слияния почты, определенную с именем, соответствующим **DataView.Table.TableName**.

Если в документе определены другие области слияния почты, они остаются нетронутыми. Это позволяет выполнять несколько операций слияния почты.

## Примеры

Показывает, как использовать регионы для выполнения двух отдельных слияний в одном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы хотим выполнить два последовательных слияния почты для одного документа, взяв данные из двух таблиц
// связаны друг с другом каким-либо образом, мы можем разделить слияния по регионам.
// Обычно MERGEFIELD содержат имя столбца источника данных слияния почты.
// Вместо этого мы можем использовать префиксы «TableStart:» и «TableEnd:» для начала/конца области слияния почты.
// Каждый регион будет принадлежать таблице с именем, соответствующим строке сразу после двоеточия префикса.
// Эти регионы являются отдельными для несвязанных данных, тогда как для иерархических данных они могут быть вложенными.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Оба MERGEFIELD ссылаются на одно и то же имя столбца, но значения для каждого будут взяты из разных таблиц данных.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Создаем две несвязанные таблицы данных.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Нам нужно будет запустить одно слияние почты на таблицу. Первое слияние почты заполнит MERGEFIELDs
// в диапазоне «Города», оставив поля диапазона «Фрукты» незаполненными.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Выполняем второе слияние для таблицы «Fruit», используя представление данных
// для сортировки строк в порядке возрастания по столбцу «Имя» перед объединением.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(*IDataReader, string*) {#executewithregions_5}

Выполняет слияние почты из**IDataReader** в документ с областями слияния почты.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataReader | IDataReader | Источник записей данных для слияния почты, таких как**OleDbDataReader** или**SqlDataReader**. |
| tableName | String | Имя области слияния в документе, которую необходимо заполнить. |

## Примечания

Вы можете пройти**SqlDataReader** или**OleDbDataReader** объект в метод this как параметр, поскольку они оба реализовали**IDataReader** интерфейс.

## Примеры

Показывает, как вставлять в отчет изображения, хранящиеся в BLOB-поле базы данных.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Откройте средство чтения данных, которое должно находиться в режиме, позволяющем считывать все записи одновременно.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Ничего не делать.
    }

    /// <summary>
    /// Вызывается, когда при слиянии почты в документе обнаруживается MERGEFIELD с тегом «Image:» в имени.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
