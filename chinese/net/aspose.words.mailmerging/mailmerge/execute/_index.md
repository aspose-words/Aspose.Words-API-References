---
title: Execute
second_title: Aspose.Words for .NET API 参考
description: 从自定义数据源执行邮件合并
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

使用此方法在文档中使用来自:::47 的值填充邮件合并字段:::任何数据源，例如列表或哈希表或对象。您需要编写自己的 类来实现[`IMailMergeDataSource`](../../imailmergedatasource)接口。

只有在[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate)为 false 时才可以使用此方法， 那就是你不需要从右到左的语言（如阿拉伯语或希伯来语）兼容性。

此方法忽略RemoveUnusedRegions选项。

### 也可以看看

* interface [IMailMergeDataSource](../../imailmergedatasource)
* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

对单个记录执行邮件合并操作。

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldNames | String[] | 合并字段名称数组。字段名称不区分大小写。 如果遇到在文档中没有找到的字段名，则忽略它。 |
| values | Object[] | 要插入到合并字段中的值数组。 此数组中的元素数必须与 fieldNames 中的元素数相同。 |

### 评论

使用此方法在文档中使用来自:::47 的值填充邮件合并字段:::对象数组。

此方法仅合并一条记录的数据。字段名称数组 和值数组表示单个记录的数据。

此方法不使用邮件合并区域。

此方法忽略RemoveUnusedRegions选项。

### 例子

显示如何将来自 URI 的图像作为邮件合并数据合并到 MERGEFIELD。

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
    Throws.TypeOf<ArgumentNullException>());  //因为HttpResponse在测试中为空而抛出。

// 我们将需要手动关闭此响应，以确保我们不会在保存后向文档添加任何多余的内容。
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

显示如何执行邮件合并，然后将文档保存到客户端浏览器。

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
    Throws.TypeOf<ArgumentNullException>());  //因为HttpResponse在测试中为空而抛出。

// 我们将需要手动关闭此响应，以确保我们不会在保存后向文档添加任何多余的内容。
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### 也可以看看

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

将数据表中的邮件合并到文档中。

```csharp
public void Execute(DataTable table)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| table | DataTable | 包含要插入邮件合并字段的数据的表。 字段名称不区分大小写。 如果遇到在文档中没有找到的字段名，则忽略它。 |

### 评论

使用此方法使用来自:::47 的值填充文档中的邮件合并字段::: **数据表** 。

表中的所有记录都合并到文档中。

您可以使用 Word 文档中的 NEXT 字段导致 **MailMerge** 对象选择 来自 **DataTable** 的下一条记录并继续合并。 这可用于创建诸如邮寄标签之类的文档。

当 **MailMerge** 对象到达主文档末尾，还有更多  **DataTable** 中的行，它复制 主文档的全部内容并将其附加到目标文档的末尾，使用一个部分 break 作为分隔符。

此方法忽略RemoveUnusedRegions选项。

### 例子

显示如何使用 DataTable 中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

     // 下面是使用DataTable作为邮件合并数据源的两种方式。
    // 1 - 使用整个表进行邮件合并，为表中的每一行创建一个输出邮件合并文档：
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

     // 2 - 使用表格的一行创建一个输出邮件合并文档：
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
 /// 创建一个邮件合并源文档。
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

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

将邮件从 IDataReader 合并到文档中。

```csharp
public void Execute(IDataReader dataReader)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataReader | IDataReader | 邮件合并操作的数据源。 |

### 评论

可以通过 **SqlDataReader** 或 **OleDbDataReader** 对象作为参数放入此 方法中，因为它们都实现了 **IDataReader** 接口。

请注意，此方法不使用邮件合并区域，对于多条记录， 文档将通过重复整个文档而增长。

此方法忽略RemoveUnusedRegions选项。

### 例子

展示如何使用来自数据阅读器的数据运行邮件合并。

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

 // 创建一个指向“Northwind”数据库的连接字符串 file
// 在我们的本地文件系统中，打开一个连接，并设置一个 SQL 查询。
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

     // 创建一个 SQL 命令，它将为我们的邮件合并获取数据。
     // 此 SELECT 语句将返回的表列的名称
     // 将需要对应于我们在上面放置的合并字段。
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

     // 这将运行命令并将数据存储在阅读器中。
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

     // 从阅读器中取出数据并在邮件合并中使用。
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### 也可以看看

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

执行从 DataView 到文档的邮件合并。

```csharp
public void Execute(DataView dataView)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataView | DataView | 邮件合并操作的数据源。 |

### 评论

如果您将数据检索到 **DataTable 中，此方法很有用** 但 需要在邮件合并之前应用过滤器或排序。

请注意，此方法不使用邮件合并区域，对于多条记录， 文档将通过重复整个文档而增长。

此方法忽略RemoveUnusedRegions选项。

### 例子

显示如何使用 DataView 编辑邮件合并数据。

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

 // 我们的数据视图沿“Grade”列以降序对条目进行排序
 // 并过滤掉该列中值小于 50 的行。
 // 四行中的三行符合这些条件，因此输出文档将包含三个合并文档。
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### 也可以看看

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

执行从 DataRow 到文档的邮件合并。

```csharp
public void Execute(DataRow row)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | DataRow | 包含要插入邮件合并字段的数据的行。 字段名称不区分大小写。 如果遇到在文档中没有找到的字段名，则忽略它。 |

### 评论

使用此方法使用来自 **的值填充文档中的邮件合并字段 数据行** 。

此方法忽略RemoveUnusedRegions选项。

### 例子

显示如何使用 DataTable 中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

     // 下面是使用DataTable作为邮件合并数据源的两种方式。
    // 1 - 使用整个表进行邮件合并，为表中的每一行创建一个输出邮件合并文档：
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

     // 2 - 使用表格的一行创建一个输出邮件合并文档：
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
 /// 创建一个邮件合并源文档。
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

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
