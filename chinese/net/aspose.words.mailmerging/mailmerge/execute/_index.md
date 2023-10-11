---
title: MailMerge.Execute
second_title: Aspose.Words for .NET API 参考
description: MailMerge 方法. 从自定义数据源执行邮件合并
type: docs
weight: 180
url: /zh/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

从自定义数据源执行邮件合并。

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | 实现自定义邮件合并数据源接口的对象。 |

### 评论

使用此方法可以使用来自 任何数据源（例如列表、哈希表或对象）的值填充文档中的邮件合并字段。您需要编写 your 自己的类来实现[`IMailMergeDataSource`](../../imailmergedatasource/)界面。

仅当以下情况时才可以使用此方法[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)是`错误的`, 即您不需要从右到左的语言（例如阿拉伯语或希伯来语）兼容性。

该方法忽略了RemoveUnusedRegions选项。

### 也可以看看

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

对单个记录执行邮件合并操作。

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。 如果遇到文档中未找到的字段名称，则会将其忽略。 |
| values | Object[] | 要插入到合并字段中的值的数组。 该数组中的元素数量必须与*fieldNames*。 |

### 评论

使用此方法可以使用 from 对象数组的值填充文档中的邮件合并字段。

此方法仅合并一条记录的数据。字段名称数组 和值数组表示单个记录的数据。

此方法不使用邮件合并区域。

该方法忽略了RemoveUnusedRegions选项。

### 例子

演示如何将 URI 中的图像作为邮件合并数据合并到 MERGEFIELD 中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 带有“Image:”标签的 MERGEFIELD 将在邮件合并期间接收图像。
// “Image:”标签中冒号后面的字符串对应于列名
// 在其单元格包含图像文件的 URI 的数据源中。
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // 创建一个数据源，其中包含我们将合并的图像的 URI。
// URI 可以是指向图像的 Web URL，也可以是图像文件的本地文件系统文件名。
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// 对一行数据源执行邮件合并。
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

演示如何执行邮件合并，然后将文档保存到客户端浏览器。

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
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //由于测试中HttpResponse为null而抛出。

// 我们需要手动关闭此响应，以确保保存后不会向文档添加任何多余的内容。
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

将数据表中的邮件合并到文档中。

```csharp
public void Execute(DataTable table)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| table | DataTable | 包含要插入邮件合并字段的数据的表。 字段名称不区分大小写。 如果遇到在文档中找不到的字段名称，则会将其忽略。 |

### 评论

使用此方法用 a 中的值填充文档中的邮件合并字段 **数据表**。

表中的所有记录都将合并到文档中。

您可以在Word文档中使用NEXT字段来引起[`MailMerge`](../)从对象中选择 下一条记录 **数据表**并继续合并。 这可以在创建邮件标签等文档时使用。

什么时候[`MailMerge`](../)对象到达主文档末尾，并且仍有 more 行 **数据表**，它复制 主文档的全部内容，并使用section 中断作为分隔符将其附加到目标文档的末尾。

该方法忽略了RemoveUnusedRegions选项。

### 例子

演示如何使用数据表中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // 下面是使用 DataTable 作为邮件合并数据源的两种方法。
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
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

执行邮件合并 **数据读取器**进入文档.

```csharp
public void Execute(IDataReader dataReader)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataReader | IDataReader | 邮件合并操作的数据源。 |

### 评论

你可以通过 **数据库读取器**或者 **OleDb数据读取器**对象作为参数传入 this 方法，因为它们都实现了 **数据读取器**界面。

请注意，此方法不使用邮件合并区域，并且对于多个记录，the 文档将通过重复整个文档来增长。

该方法忽略了RemoveUnusedRegions选项。

### 例子

演示如何使用数据读取器中的数据运行邮件合并。

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

// 创建一个指向“Northwind”数据库文件的连接字符串
// 在我们的本地文件系统中，打开一个连接，并设置一个 SQL 查询。
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // 创建一个 SQL 命令，为我们的邮件合并提供数据源。
    // 此 SELECT 语句将返回的表列的名称
    // 需要对应于我们上面放置的合并字段。
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {                    
        connection.Open();                 
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            // 从阅读器获取数据并在邮件合并中使用它。
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
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

从 a 执行邮件合并 **数据视图**进入文档.

```csharp
public void Execute(DataView dataView)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataView | DataView | 邮件合并操作的数据源。 |

### 评论

如果您将数据检索到 **数据表**但 then 需要在邮件合并之前应用过滤器或排序。

请注意，此方法不使用邮件合并区域，并且对于多个记录，the 文档将通过重复整个文档来增长。

该方法忽略了RemoveUnusedRegions选项。

### 例子

演示如何使用 DataView 编辑邮件合并数据。

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

// 我们可以使用数据视图来更改邮件合并数据，而无需更改数据表本身。
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// 我们的数据视图沿着“Grade”列按降序对条目进行排序
// 并过滤掉该列上值小于 50 的行。
// 四行中的三行符合这些条件，因此输出文档将包含三个合并文档。
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

从 a 执行邮件合并 **数据行**进入文档.

```csharp
public void Execute(DataRow row)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | DataRow | 包含要插入邮件合并字段的数据的行。 字段名称不区分大小写。 如果遇到在文档中找不到的字段名称，则会将其忽略。 |

### 评论

使用此方法可以使用来自某个文档的值填充文档中的邮件合并字段。 **数据行**。

该方法忽略了RemoveUnusedRegions选项。

### 例子

演示如何使用数据表中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // 下面是使用 DataTable 作为邮件合并数据源的两种方法。
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
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)


