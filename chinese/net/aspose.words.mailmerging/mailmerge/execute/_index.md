---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words for .NET
description: 使用 MailMerge Execute 方法简化您的邮寄流程，轻松合并来自自定义来源的数据以实现个性化通信。
type: docs
weight: 180
url: /zh/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

从自定义数据源执行邮件合并。

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | 实现自定义邮件合并数据源接口的对象。 |

## 评论

使用此方法可以将来自任何数据源（例如列表、哈希表或对象）的值填充到文档中的邮件合并字段中。您需要编写您自己的类来实现[`IMailMergeDataSource`](../../imailmergedatasource/)界面。

仅当以下情况时才可以使用此方法[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)是`错误的`, 也就是说您不需要从右到左的语言（例如阿拉伯语或希伯来语）兼容性。

此方法忽略RemoveUnusedRegions选项。

## 例子

展示如何以自定义对象的形式执行与数据源的邮件合并。

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

     // 要使用自定义对象作为数据源，它必须实现 IMailMergeDataSource 接口。
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
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
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
 /// 您实现的自定义邮件合并数据源，以允许 Aspose.Words
/// 将客户对象中的数据通过邮件合并到 Microsoft Word 文档中。
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
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
        get { return "Customer"; }
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

### 也可以看看

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

对单个记录执行邮件合并操作。

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。 如果遇到文档中未找到的字段名称，则忽略该字段名称。 |
| values | Object[] | 要插入到合并字段的值数组。 此数组中的元素数必须与*fieldNames*。 |

## 评论

使用此方法用来自 对象数组的值填充文档中的邮件合并字段。

此方法仅合并一条记录的数据。字段 names 数组和 values 数组表示单条记录的数据。

此方法不使用邮件合并区域。

此方法忽略RemoveUnusedRegions选项。

## 例子

展示如何将 URI 中的图像作为邮件合并数据合并到 MERGEFIELD 中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 带有“Image:”标签的 MERGEFIELD 将在邮件合并期间接收图像。
// “Image:”标签中冒号后的字符串对应一个列名
// 在单元格包含图像文件 URI 的数据源中。
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // 创建一个包含我们将要合并的图像的 URI 的数据源。
// URI 可以是指向图像的 Web URL，也可以是图像文件的本地文件系统文件名。
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// 对具有一行的数据源执行邮件合并。
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

展示如何执行邮件合并，然后将文档保存到客户端浏览器。

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

// 将文档发送到客户端浏览器。
//由于测试中 HttpResponse 为空而抛出。
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// 我们需要手动关闭此响应，以确保保存后不会向文档添加任何多余的内容。
Assert.Throws<NullReferenceException>(() => response.End());
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

将 DataTable 中的邮件合并到文档中。

```csharp
public void Execute(DataTable table)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| table | DataTable | 包含要插入邮件合并字段的数据的表。 字段名称不区分大小写。 如果遇到文档中未找到的字段名称，则会忽略该字段名称。 |

## 评论

使用此方法使用 a 中的值填充文档中的邮件合并字段**数据表**。

表中的所有记录都合并到文档中。

您可以使用 Word 文档中的 NEXT 字段来[`MailMerge`](../)对象从 select 中选择下一个记录**数据表**并继续合并。 这可用于创建邮寄标签等文档。

什么时候[`MailMerge`](../)对象到达主文档末尾，并且仍有 more 行**数据表**，它复制主文档的全部内容并将其附加到目标文档的末尾，使用 section 分隔符作为分隔符。

此方法忽略RemoveUnusedRegions选项。

## 例子

展示如何使用 DataTable 中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // 以下是使用 DataTable 作为邮件合并数据源的两种方法。
    // 1 - 使用整个表进行邮件合并，为表中的每一行创建一个输出邮件合并文档：
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - 使用表的一行创建一个输出邮件合并文档：
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// 创建邮件合并源文档。
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

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

执行邮件合并**数据读取器**进入文档。

```csharp
public void Execute(IDataReader dataReader)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataReader | IDataReader | 邮件合并操作的数据源。 |

## 评论

你可以通过**SqlDataReader**或者**OleDb数据读取器**对象作为参数放入 this 方法中，因为它们都实现了**数据读取器**界面。

请注意，此方法不使用邮件合并区域，并且对于多条记录， 文档将通过重复整个文档而增长。

此方法忽略RemoveUnusedRegions选项。

## 例子

展示如何使用数据读取器中的数据运行邮件合并。

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

// 创建指向“Northwind”数据库文件的连接字符串
// 在我们的本地文件系统中，打开一个连接，并设置一个 SQL 查询。
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // 创建一个 SQL 命令，为我们的邮件合并提供数据。
    // 此 SELECT 语句将返回的表列的名称
    // 需要与我们上面放置的合并字段相对应。
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {
        connection.Open();
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // 从阅读器中获取数据并在邮件合并中使用它。
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

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

从**数据视图**进入文档。

```csharp
public void Execute(DataView dataView)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataView | DataView | 邮件合并操作的数据源。 |

## 评论

如果您将数据检索到**数据表**但 then 需要在邮件合并之前应用过滤器或排序。

请注意，此方法不使用邮件合并区域，并且对于多条记录， 文档将通过重复整个文档而增长。

此方法忽略RemoveUnusedRegions选项。

## 例子

展示如何使用 DataView 编辑邮件合并数据。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// 创建一个数据表，我们的邮件合并将从中获取数据。
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// 我们可以使用数据视图来改变邮件合并数据，而无需更改数据表本身。
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// 我们的数据视图按照“等级”列的降序对条目进行排序
// 并过滤掉该列中值小于 50 的行。
// 四行中有三行符合这些条件，因此输出文档将包含三个合并文档。
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

从**数据行**进入文档。

```csharp
public void Execute(DataRow row)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | DataRow | 包含要插入邮件合并字段的数据的行。 字段名称不区分大小写。 如果遇到文档中未找到的字段名称，则会忽略该字段名称。 |

## 评论

使用此方法使用来自**数据行**。

此方法忽略RemoveUnusedRegions选项。

## 例子

展示如何使用 DataTable 中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // 以下是使用 DataTable 作为邮件合并数据源的两种方法。
    // 1 - 使用整个表进行邮件合并，为表中的每一行创建一个输出邮件合并文档：
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - 使用表的一行创建一个输出邮件合并文档：
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// 创建邮件合并源文档。
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

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
