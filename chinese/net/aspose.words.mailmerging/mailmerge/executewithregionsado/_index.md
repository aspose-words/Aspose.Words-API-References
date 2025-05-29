---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: Aspose.Words for .NET
description: 使用 MailMerge ExecuteWithRegionsADO 方法简化文档创建。轻松合并 ADO 记录集数据，获得个性化结果。
type: docs
weight: 210
url: /zh/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

使用邮件合并区域执行从 ADO Recordset 对象到文档的邮件合并。

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| recordset | Object | ADO 记录集或记录对象。 |
| tableName | String | 文档中要填充的邮件合并区域的名称。 |

## 评论

当您打算从非托管代码（例如使用 ASP 或 Visual Basic 6.0 构建的应用程序）中使用 Aspose.Words 类作为 COM 对象时，此方法很有用。

有关详细信息，请参阅[`ExecuteWithRegions`](../executewithregions/)。

## 例子

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

展示如何运行包含多个区域的邮件合并，并使用来自 ADO 数据集的数据进行编译。

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // 要使用 ADO DataSets，我们需要添加对 Microsoft ActiveX Data Objects 库的引用，
    // 包含在 .NET 分发中并存储在“adodb.dll”中。
    ADODB.Connection connection = new ADODB.Connection();

    // 创建指向“Northwind”数据库文件的连接字符串
    // 在我们的本地文件系统中并打开连接。
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // 通过在我们的数据库上运行 SQL 命令来填充我们的数据集。
    // 结果表中的列名需要对应
    // 到将容纳我们的数据的 MERGEFIELDS 的值。
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // 仅在第一个区域上运行邮件合并，并使用记录集中的数据填充其 MERGEFIELDS。
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // 关闭记录集并使用来自另一个 SQL 查询的数据重新打开它。
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // 在第二个区域运行第二个邮件合并并保存文档。
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
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
