---
title: MailMerge.ExecuteWithRegions
linktitle: ExecuteWithRegions
articleTitle: ExecuteWithRegions
second_title: Aspose.Words for .NET
description: 使用 MailMerge ExecuteWithRegions 方法简化文档创建，实现来自自定义数据源和区域的高效邮件合并。
type: docs
weight: 200
url: /zh/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#executewithregions}

使用邮件合并区域从自定义数据源执行邮件合并。

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | 实现自定义邮件合并数据源接口的对象。 |

## 评论

使用此方法，可以使用来自任何自定义数据源（例如 XML 文件或业务对象集合）的值填充文档中的邮件合并字段。您需要编写您自己的类来实现[`IMailMergeDataSource`](../../imailmergedatasource/)界面。

仅当以下情况时才可以使用此方法[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)是`错误的`, 也就是说您不需要从右到左的语言（例如阿拉伯语或希伯来语）兼容性。

## 例子

展示如何使用邮件合并区域执行嵌套邮件合并。

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 通常，MERGEFIELD 包含邮件合并数据源的列的名称。
    // 相反，我们可以使用“TableStart：”和“TableEnd：”前缀来开始/结束邮件合并区域。
    // 每个区域都属于一个表，其名称与前缀冒号后面的字符串匹配。
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // 这些 MERGEFIELD 位于“客户”表的邮件合并区域内。
    // 当我们执行邮件合并时，该字段将从名为“客户”的数据源中的行接收数据。
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // 在外部区域内为名为“Orders”的数据源创建第二个邮件合并区域。
    // “订单”数据条目与“客户”数据源具有多对一的关系。
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // 创建名称与我们的邮件合并区域相匹配的相关数据。
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // 要从数据源进行邮件合并，我们必须将其包装到实现 IMailMergeDataSource 接口的对象中。
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// 您的应用程序中“数据实体”类的示例。
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
/// 包含“数据”对象的类型集合的示例。
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
/// 应用程序中子“数据实体”类的示例。
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
 /// 您实现的自定义邮件合并数据源，以允许 Aspose.Words
/// 将客户对象中的数据通过邮件合并到 Microsoft Word 文档中。
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // 当我们初始化数据源时，它的位置必须在第一个记录之前。
        mRecordIndex = -1;
    }

    /// <summary>
    /// 数据源的名称。仅在执行可重复区域的邮件合并时由 Aspose.Words 使用。
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
    }

    /// <summary>
    /// Aspose.Words 调用此方法来获取每个数据字段的值。
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
                // 返回“false”给 Aspose.Words 邮件合并引擎以表示
                // 我们找不到具有此名称的字段。
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// 移动到集合中的下一个记录的标准实现。
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
            // 获取子数据源，其名称与使用其列的邮件合并区域匹配。
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

        // 当我们初始化数据源时，它的位置必须在第一个记录之前。
        mRecordIndex = -1;
    }

    /// <summary>
    /// 数据源的名称。仅在执行可重复区域的邮件合并时由 Aspose.Words 使用。
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words 调用此方法来获取每个数据字段的值。
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
                // 返回“false”给 Aspose.Words 邮件合并引擎以表示
                // 我们找不到具有此名称的字段。
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// 移动到集合中的下一个记录的标准实现。
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    /// <summary>
    /// 返回 null 因为我们没有这种对象的任何子元素。
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

### 也可以看看

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*[IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)*) {#executewithregions_1}

使用邮件合并区域从自定义数据源执行邮件合并。

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | 实现自定义邮件合并数据源根接口的对象。 |

## 评论

使用此方法，可以使用来自任何自定义数据源（例如 XML 文件或业务对象集合）的值填充文档中的邮件合并字段。您需要编写自己的类来实现[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/)和[`IMailMergeDataSource`](../../imailmergedatasource/)接口。

仅当以下情况时才可以使用此方法[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)是`错误的`, 也就是说您不需要从右到左的语言（例如阿拉伯语或希伯来语）兼容性。

## 例子

从具有主从数据的自定义数据源执行邮件合并。

```csharp
public void CustomDataSourceRoot()
{
    // 创建一个包含两个邮件合并区域的文档，分别名为“华盛顿”和“西雅图”。
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // 为邮件合并创建两个数据源。
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // 在数据源根中按名称注册我们的数据源。
    // 如果我们要在与区域邮件合并中使用此数据源根，
    // 每个源的注册名称必须与邮件合并源文档中现有邮件合并区域的名称相匹配。
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // 由于我们有连续的邮件合并区域，因此我们通常必须执行两次邮件合并。
    // 但是，一个具有数据根的邮件合并源可以填充多个区域
    // 如果根包含具有相应名称/列名的表。
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// 创建一个包含连续邮件合并区域的文档，其名称由输入数组指定，
/// 用于员工数据表。
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
/// 您的应用程序中“数据实体”类的示例。
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
/// 包含“数据”对象的类型集合的示例。
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
/// 可以直接传递到邮件合并中的数据源根，该邮件合并可以注册并包含许多子数据源。
/// 这些源都必须实现 IMailMergeDataSource，并通过名称进行注册和区分
/// 对应于将读取相应数据的邮件合并区域。
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
/// 自定义邮件合并数据源。
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
    }

    /// <summary>
    /// 移动到集合中的下一个记录的标准实现。
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
    /// 数据源的名称。仅在执行可重复区域的邮件合并时由 Aspose.Words 使用。
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words 调用此方法来获取每个数据字段的值。
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
                // 返回“false”给 Aspose.Words 邮件合并引擎以表示
                // 我们找不到具有此名称的字段。
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// 子数据源用于嵌套邮件合并。
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### 也可以看看

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataSet*) {#executewithregions_2}

从**数据集**到带有邮件合并区域的文档中。

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSet | DataSet | **数据集**包含要插入邮件合并字段的数据。 |

## 评论

使用此方法可将一个或多个表格中的邮件合并到文档中可重复的邮件合并区域中。文档内的邮件合并区域将动态增长以容纳相应表格中的记录。

每张桌子**数据集**一定有名字。

文档必须具有定义在名称中引用 table 的邮件合并区域**数据集**。

要在文档中指定邮件合并区域，您需要插入两个邮件合并字段 来标记邮件合并区域的开始和结束。

邮件合并区域内包含的所有文档内容将自动 重复用于邮件合并区域中的每条记录**数据表**。

要标记邮件合并区域的开始，请插入名为 TableStart:MyTable, 的 MERGEFIELD，其中 MyTable 对应于您的**数据集**。

要标记邮件合并区域的结束，请插入另一个名为 TableEnd:MyTable 的 MERGEFIELD。

要在 Word 中插入 MERGEFIELD，请使用“插入/字段”命令并选择“合并字段”，然后键入字段的 the 名称。

这**表开始**和**桌尾**字段必须位于文档的同一部分内。

如果在表格中使用，**表开始**和**桌尾**必须位于表中的同一行内。

文档中的邮件合并区域应格式正确（总是需要一对匹配的 **表开始**和**桌尾**合并具有相同表名的字段）。

## 例子

展示如何使用两个合并区域和两个数据表执行嵌套邮件合并。

```csharp
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 通常，MERGEFIELD 包含邮件合并数据源的列的名称。
    // 相反，我们可以使用“TableStart：”和“TableEnd：”前缀来开始/结束邮件合并区域。
    // 每个区域都属于一个表，其名称与前缀冒号后面的字符串匹配。
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // 此 MERGEFIELD 位于“客户”表的邮件合并区域内。
    // 当我们执行邮件合并时，该字段将从名为“客户”的数据源中的行接收数据。
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // 为包含来自第二个内部区域的值的表创建列标题。
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // 在外部区域内为名为“Orders”的表创建第二个邮件合并区域。
    // “订单”表与“客户”表在“客户 ID”列上具有多对一关系。
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // 结束内部区域，然后结束外部区域。邮件合并区域的打开和关闭必须
    // 发生在表的同一行上。
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // 创建一个包含具有所需名称和关系的两个表的数据集。
    // 外部合并区域的“客户”表的每一行的每个合并文档将在“订单”表上执行其邮件合并。
    // 每个合并文档将显示后一个表中“CustomerID”列值与当前“Customers”表行匹配的所有行。
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// 生成一个数据集，其中包含两个数据表，分别为“客户”和“订单”，并且在“客户 ID”列上具有一对多关系。
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

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataTable*) {#executewithregions_3}

从**数据表**放入带有邮件合并区域的文档中。

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataTable | DataTable | 邮件合并操作的数据源。表 must 有其TableName属性集。 |

## 评论

文档必须具有一个定义为 matches 名称的邮件合并区域TableName。

如果文档中定义了其他邮件合并区域，则它们将保持不变。 这允许执行多个邮件合并操作。

## 例子

演示如何在邮件合并期间设置单元格格式。

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
/// 当邮件合并发生时，将表格行格式化为在奇数行/偶数行上交替两种颜色。
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// 当邮件合并将数据合并到 MERGEFIELD 时调用。
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // 如果我们在第一列，情况确实如此，这意味着我们已经移动到新行。
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
        // 什么也不做。
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Visual Basic 自动移植所需的函数，用于返回传递数字的奇偶校验。
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// 创建邮件合并数据源。
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

展示如何使用区域在一个文档中执行两个单独的邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果我们想在一个文档上执行两次连续的邮件合并，同时从两个表中获取数据
// 以任何方式相互关联，我们可以将邮件合并与区域分开。
// 通常，MERGEFIELD 包含邮件合并数据源的列的名称。
// 相反，我们可以使用“TableStart：”和“TableEnd：”前缀来开始/结束邮件合并区域。
// 每个区域都属于一个表，其名称与前缀冒号后面的字符串匹配。
// 对于不相关的数据，这些区域是分开的，而对于分层数据，它们可以嵌套。
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// 两个 MERGEFIELD 都引用相同的列名，但每个值都来自不同的数据表。
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// 创建两个不相关的数据表。
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

// 我们需要为每个表运行一次邮件合并。第一次邮件合并将填充合并字段
// 在“城市”范围内，同时将“水果”范围的字段留空。
doc.MailMerge.ExecuteWithRegions(tableCities);

// 使用数据视图对“Fruit”表运行第二次合并
// 在合并之前按“名称”列的升序对行进行排序。
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*DataView*) {#executewithregions_4}

从**数据视图**放入带有邮件合并区域的文档中。

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataView | DataView | 邮件合并操作的数据源。**数据视图**必须有其**表名**属性集。 |

## 评论

如果您将数据检索到**数据表**但 then 需要在邮件合并之前应用过滤器或排序。

文档必须具有一个定义为 matches 名称的邮件合并区域**数据视图.表.表名称**。

如果文档中定义了其他邮件合并区域，则它们将保持不变。 这允许执行多个邮件合并操作。

## 例子

展示如何使用区域在一个文档中执行两个单独的邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 如果我们想在一个文档上执行两次连续的邮件合并，同时从两个表中获取数据
// 以任何方式相互关联，我们可以将邮件合并与区域分开。
// 通常，MERGEFIELD 包含邮件合并数据源的列的名称。
// 相反，我们可以使用“TableStart：”和“TableEnd：”前缀来开始/结束邮件合并区域。
// 每个区域都属于一个表，其名称与前缀冒号后面的字符串匹配。
// 对于不相关的数据，这些区域是分开的，而对于分层数据，它们可以嵌套。
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// 两个 MERGEFIELD 都引用相同的列名，但每个值都来自不同的数据表。
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// 创建两个不相关的数据表。
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

// 我们需要为每个表运行一次邮件合并。第一次邮件合并将填充合并字段
// 在“城市”范围内，同时将“水果”范围的字段留空。
doc.MailMerge.ExecuteWithRegions(tableCities);

// 使用数据视图对“Fruit”表运行第二次合并
// 在合并之前按“名称”列的升序对行进行排序。
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## ExecuteWithRegions(*IDataReader, string*) {#executewithregions_5}

执行邮件合并**数据读取器**放入带有邮件合并区域的文档中。

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataReader | IDataReader | 邮件合并的数据记录来源，例如**OleDb数据读取器**或者**SqlDataReader**。 |
| tableName | String | 文档中要填充的邮件合并区域的名称。 |

## 评论

你可以通过**SqlDataReader**或者**OleDb数据读取器**对象作为参数放入 this 方法中，因为它们都实现了**数据读取器**界面。

## 例子

展示如何将存储在数据库 BLOB 字段中的图像插入到报告中。

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

        // 打开数据读取器，需要处于一次读取所有记录的模式。
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
        // 什么也不做。
    }

    /// <summary>
    /// 当邮件合并在文档中遇到名称中带有“Image:”标签的 MERGEFIELD 时调用此函数。
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
