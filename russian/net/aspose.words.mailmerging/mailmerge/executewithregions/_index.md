---
title: ExecuteWithRegions
second_title: Справочник по API Aspose.Words для .NET
description: Выполняет слияние из пользовательского источника данных с областями слияния.
type: docs
weight: 200
url: /ru/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

Выполняет слияние из пользовательского источника данных с областями слияния.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Объект, реализующий настраиваемый интерфейс источника данных для слияния почты. |

### Примечания

Используйте этот метод, чтобы заполнить поля слияния в документе значениями from из любого пользовательского источника данных, такого как файл XML или коллекции бизнес-объектов. Вам нужно написать собственный класс your , реализующий[`IMailMergeDataSource`](../../imailmergedatasource) интерфейс.

Вы можете использовать этот метод только тогда, когда[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate)ложно, то есть вам не нужна совместимость с языками с письмом справа налево (такими как арабский или иврит).

### Примеры

Показывает, как использовать области слияния для выполнения вложенного слияния.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Обычно поля MERGEFIELD содержат имя столбца источника данных слияния.
    // Вместо этого мы можем использовать префиксы "TableStart:" и "TableEnd:" для начала/завершения области слияния.
    // Каждый регион будет принадлежать таблице с именем, которое соответствует строке сразу после двоеточия префикса.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Эти поля MERGEFIELD находятся внутри области слияния почты таблицы «Клиенты».
    // Когда мы выполним слияние, это поле будет получать данные из строк в источнике данных с именем «Клиенты».
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Создайте вторую область слияния внутри внешней области для источника данных с именем «Заказы».
    // Записи данных «Заказы» имеют отношение «многие к одному» с источником данных «Клиенты».
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Создать связанные данные с именами, соответствующими именам наших регионов слияния.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Чтобы слить почту из вашего источника данных, мы должны обернуть его в объект, который реализует интерфейс IMailMergeDataSource.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Пример класса "объект данных" в вашем приложении.
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
/// Пример типизированной коллекции, содержащей ваши объекты "данные".
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
/// Пример дочернего класса "сущности данных" в вашем приложении.
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
/// Пользовательский источник данных слияния, который вы реализуете, чтобы позволить Aspose.Words 
/// для отправки данных слияния из ваших объектов Customer в документы Microsoft Word.
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
    /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяемыми областями.
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
                // Возвращаем "false" механизму слияния почты Aspose.Words, чтобы обозначить
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
            // Получить дочерний источник данных, имя которого соответствует области слияния, в которой используются его столбцы.
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
    /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяемыми областями.
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
                // Возвращаем "false" механизму слияния почты Aspose.Words, чтобы обозначить
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
    /// Возвращаем null, потому что у нас нет дочерних элементов для объектов такого типа.
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

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(IMailMergeDataSourceRoot) {#executewithregions_1}

Выполняет слияние из пользовательского источника данных с областями слияния.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Объект, реализующий настраиваемый корневой интерфейс источника данных слияния. |

### Примечания

Используйте этот метод, чтобы заполнить поля слияния в документе значениями from из любого пользовательского источника данных, такого как файл XML или коллекции бизнес-объектов. Вам нужно написать свои собственные классы , которые реализуют[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot) а также[`IMailMergeDataSource`](../../imailmergedatasource) интерфейсы.

Вы можете использовать этот метод только тогда, когда[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate)ложно, то есть вам не нужна совместимость с языками с письмом справа налево (такими как арабский или иврит).

### Примеры

Выполняет слияние почты из пользовательского источника данных с основными и подробными данными.

```csharp
public void CustomDataSourceRoot()
{
    // Создайте документ с двумя областями слияния с именами «Вашингтон» и «Сиэтл».
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Создадим два источника данных для слияния.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Регистрируем наши источники данных по имени в корне источника данных.
    // Если мы собираемся использовать этот корень источника данных в почтовом слиянии с регионами,
    // зарегистрированное имя каждого источника должно совпадать с именем существующей области слияния в исходном документе слияния.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Так как у нас есть последовательные регионы слияния, обычно нам приходится выполнять два слияния.
    // Однако один источник слияния с корнем данных может заполнять несколько регионов
    // если в корне есть таблицы с соответствующими именами/именами столбцов.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Создать документ, содержащий последовательные области слияния с именами, указанными во входном массиве,
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
/// Пример класса "объект данных" в вашем приложении.
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
/// Пример типизированной коллекции, содержащей ваши объекты "данные".
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
/// Корень источника данных, который можно передать непосредственно в слияние, которое может регистрироваться и содержать множество дочерних источников данных.
/// Все эти источники должны реализовывать IMailMergeDataSource, они зарегистрированы и различаются по имени
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
/// Пользовательский источник данных слияния почты.
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
    /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяемыми областями.
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
                // Возвращаем "false" механизму слияния почты Aspose.Words, чтобы обозначить
                // что мы не смогли найти поле с таким именем.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Дочерние источники данных предназначены для вложенных слияний почты.
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

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot)
* class [MailMerge](../../mailmerge)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataSet) {#executewithregions_2}

Выполняет слияние из набора данных в документ с областями слияния.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSet | DataSet | Набор данных, содержащий данные для вставки в поля слияния. |

### Примечания

Используйте этот метод для выполнения слияния почты из одной или нескольких таблиц в повторяющиеся области слияния mail в документе. Области слияния внутри документа будут динамически увеличиваться для размещения записей в соответствующих таблицах.

Каждая таблица в наборе данных должна иметь имя.

В документе должны быть определены области слияния с именами, которые ссылаются на таблицы в наборе данных.

Чтобы указать область слияния в документе, вам нужно вставить два поля слияния , чтобы отметить начало и конец области слияния.

Все содержимое документа, включенного в область слияния, будет автоматически повторяться для каждой записи в DataTable.

Чтобы отметить начало области слияния, вставьте MERGEFIELD с именем TableStart:MyTable, , где MyTable соответствует одному из имен таблиц в вашем наборе данных.

Чтобы отметить конец области слияния, вставьте еще одно поле MERGEFIELD с именем TableEnd:MyTable.

Чтобы вставить MERGEFIELD в Word, используйте команду Insert/Field и выберите MergeField, затем введите имя поля .

Поля TableStart и TableEnd должны находиться в одном и том же разделе документа.

При использовании внутри таблицы TableStart и TableEnd должны находиться в одной и той же строке таблицы.

Области слияния в документе должны быть правильно сформированы (всегда должна быть пара совпадающих полей слияния TableStart и TableEnd с одинаковым именем таблицы).

### Примеры

Показывает, как выполнить вложенное слияние почты с двумя областями слияния и двумя таблицами данных.

```csharp
[Test]
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Обычно поля MERGEFIELD содержат имя столбца источника данных слияния.
    // Вместо этого мы можем использовать префиксы "TableStart:" и "TableEnd:" для начала/завершения области слияния.
    // Каждый регион будет принадлежать таблице с именем, которое соответствует строке сразу после двоеточия префикса.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Это поле MERGEFIELD находится внутри области слияния почты таблицы «Клиенты».
    // Когда мы выполним слияние, это поле будет получать данные из строк в источнике данных с именем «Клиенты».
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

    // Создайте вторую область слияния внутри внешней области для таблицы с именем «Заказы».
    // Таблица «Заказы» имеет связь «многие к одному» с таблицей «Клиенты» в столбце «Код клиента».
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Конец внутренней области, а затем конец внешней области. Открытие и закрытие области слияния должно
    // происходят в той же строке таблицы.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Создайте набор данных, содержащий две таблицы с требуемыми именами и отношениями.
    // Каждый документ слияния для каждой строки таблицы «Клиенты» внешней области слияния будет выполнять слияние почты в таблице «Заказы».
    // Каждый документ слияния будет отображать все строки последней таблицы, значения столбца «CustomerID» которых соответствуют текущей строке таблицы «Customers».
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Генерирует набор данных, содержащий две таблицы данных с именами «Клиенты» и «Заказы» с отношением «один ко многим» в столбце «CustomerID».
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

* class [MailMerge](../../mailmerge)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataTable) {#executewithregions_3}

Выполняет слияние из DataTable в документ с областями слияния.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataTable | DataTable | Источник данных для операции слияния почты. Таблица должна иметь свой **ИмяТаблицы** набор свойств. |

### Примечания

В документе должна быть определена область слияния с именем, соответствующим  **DataTable.TableName**.

Если в документе определены другие области слияния, они остаются нетронутыми. Это позволяет выполнять несколько операций слияния.

### Примеры

Демонстрирует, как форматировать ячейки во время слияния.

```csharp
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");

/// <summary>
/// Форматирует строки таблицы по мере того, как происходит слияние почты, чтобы чередовать два цвета в нечетных/четных строках.
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
/// Создает источник данных слияния почты.
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

Показывает, как использовать регионы для выполнения двух отдельных слияний почты в одном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы хотим выполнить два последовательных слияния почты в одном документе, взяв данные из двух таблиц
// связаны друг с другом каким-либо образом, мы можем разделить почтовые слияния с регионами.
// Обычно поля MERGEFIELD содержат имя столбца источника данных слияния.
// Вместо этого мы можем использовать префиксы "TableStart:" и "TableEnd:" для начала/завершения области слияния.
// Каждый регион будет принадлежать таблице с именем, которое соответствует строке сразу после двоеточия префикса.
// Эти области являются отдельными для несвязанных данных, а для иерархических данных они могут быть вложены друг в друга.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Оба MERGEFIELD относятся к одному и тому же имени столбца, но значения для каждого из них будут поступать из разных таблиц данных.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Создадим две несвязанные таблицы данных.
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

// Нам нужно будет выполнить одно слияние почты для каждой таблицы. Первое слияние почты заполнит поля MERGEFIELD.
// в диапазоне "Города", оставив поля диапазона "Фрукты" незаполненными.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Запускаем второе слияние для таблицы Fruit, используя представление данных
// для сортировки строк по возрастанию в столбце "Имя" перед слиянием.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Смотрите также

* class [MailMerge](../../mailmerge)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataView) {#executewithregions_4}

Выполняет слияние почты из DataView в документ с областями слияния.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataView | DataView | Источник данных для операции слияния почты. Исходная таблица файла **Просмотр данных** должен иметь свой **ИмяТаблицы** набор свойств. |

### Примечания

Этот метод полезен, если вы извлекаете данные в **Таблица данных** но тогда нужно применять фильтр или сортировать перед слиянием почты.

В документе должна быть определена область слияния с именем, соответствующим  **DataView.Table.TableName**.

Если в документе определены другие области слияния, они остаются нетронутыми. Это позволяет выполнять несколько операций слияния.

### Примеры

Показывает, как использовать регионы для выполнения двух отдельных слияний почты в одном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы хотим выполнить два последовательных слияния почты в одном документе, взяв данные из двух таблиц
// связаны друг с другом каким-либо образом, мы можем разделить почтовые слияния с регионами.
// Обычно поля MERGEFIELD содержат имя столбца источника данных слияния.
// Вместо этого мы можем использовать префиксы "TableStart:" и "TableEnd:" для начала/завершения области слияния.
// Каждый регион будет принадлежать таблице с именем, которое соответствует строке сразу после двоеточия префикса.
// Эти области являются отдельными для несвязанных данных, а для иерархических данных они могут быть вложены друг в друга.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Оба MERGEFIELD относятся к одному и тому же имени столбца, но значения для каждого из них будут поступать из разных таблиц данных.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Создадим две несвязанные таблицы данных.
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

// Нам нужно будет выполнить одно слияние почты для каждой таблицы. Первое слияние почты заполнит поля MERGEFIELD.
// в диапазоне "Города", оставив поля диапазона "Фрукты" незаполненными.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Запускаем второе слияние для таблицы Fruit, используя представление данных
// для сортировки строк по возрастанию в столбце "Имя" перед слиянием.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Смотрите также

* class [MailMerge](../../mailmerge)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge)
* сборка [Aspose.Words](../../../)

---

## ExecuteWithRegions(IDataReader, string) {#executewithregions_5}

Выполняет слияние почты из IDataReader в документ с областями слияния.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataReader | IDataReader | Источник записей данных для слияния, например OleDbDataReader или SqlDataReader. |
| tableName | String | Имя области слияния в документе для заполнения. |

### Примечания

Вы можете пройти **SqlDataReader** или же **Оледбдатаридер** объект в метод this в качестве параметра, потому что они оба реализовали **IDataReader** интерфейс.

### Примеры

Показывает, как вставить изображения, хранящиеся в поле BLOB базы данных, в отчет.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Откройте средство чтения данных, которое должно быть в режиме чтения всех записей одновременно.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Ничего не делать.
    }

    /// <summary>
    /// Это вызывается, когда слияние встречает MERGEFIELD в документе с тегом «Image:» в его имени.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Смотрите также

* class [MailMerge](../../mailmerge)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
