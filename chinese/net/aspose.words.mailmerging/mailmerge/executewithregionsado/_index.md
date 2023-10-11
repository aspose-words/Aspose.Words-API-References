---
title: MailMerge.ExecuteWithRegionsADO
second_title: Aspose.Words for .NET API 参考
description: MailMerge 方法. 将 ADO Recordset 对象的邮件合并到具有邮件合并区域的文档中
type: docs
weight: 210
url: /zh/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

将 ADO Recordset 对象的邮件合并到具有邮件合并区域的文档中。

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| recordset | Object | ADO 记录集或记录对象。 |
| tableName | String | 文档中要填充的邮件合并区域的名称。 |

### 评论

当您打算使用非托管代码中的 Aspose.Words 类 as COM 对象（例如使用 ASP 或 Visual Basic 6.0 构建的应用程序）时，此方法非常有用。

欲了解更多信息，请参阅描述[`ExecuteWithRegions`](../executewithregions/)。

### 例子

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT * FROM AsposeWordOrderDetails WHERE OrderId = 10444 ORDER BY ProductID", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")

Dim Doc
Set Doc = Helper.Open("Invoice.doc")

Doc.MailMerge.ExecuteWithRegionsADO RS, "OrderDetails"
Doc.Save "Invoice Out VBScript.doc"
```

演示如何运行多个区域的邮件合并，并使用 ADO 数据集中的数据进行编译。

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // 要使用 ADO 数据集，我们需要添加对 Microsoft ActiveX 数据对象库的引用，
    // 它包含在 .NET 发行版中并存储在“adodb.dll”中。
    ADODB.Connection connection = new ADODB.Connection();

    // 创建一个指向“Northwind”数据库文件的连接字符串
    // 在我们的本地文件系统中并打开一个连接。
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // 通过在数据库上运行 SQL 命令来填充我们的数据集。
    // 结果表中的列名需要对应
    // 将容纳我们的数据的 MERGEFIELDS 的值。
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // 仅在第一个区域上运行邮件合并，用记录集中的数据填充其 MERGEFIELDS。
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // 关闭记录集并使用另一个 SQL 查询中的数据重新打开它。
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // 在第二个区域上运行第二次邮件合并并保存文档。
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// 创建一个包含两个邮件合并区域的文档。
/// </summary>
private static Document CreateSourceDocADOMailMergeWithRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("\tEmployees: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion1");
    builder.InsertField(" MERGEFIELD FirstName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD LastName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion1");
    builder.InsertParagraph();

    builder.Writeln("\tCustomers: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion2");
    builder.InsertField(" MERGEFIELD ContactName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Address");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion2");

    return doc;
}
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../mailmerge/)
* 部件 [Aspose.Words](../../../)


