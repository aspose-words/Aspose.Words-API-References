---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: 用于 .NET 的 Aspose.Words
description: MailMerge ExecuteADO 方法. 执行从 ADO Recordset 对象到文档的邮件合并 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

执行从 ADO Recordset 对象到文档的邮件合并。

```csharp
public void ExecuteADO(object recordset)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| recordset | Object | ADO 记录集或记录对象。 |

## 评论

当您打算从非托管代码（例如使用 ASP 或Visual Basic 6.0 构建的应用程序）中使用Aspose.Words 类as COM 对象时，此方法很有用。

此方法忽略RemoveUnusedRegions选项。

有关详细信息，请参阅 MailMerge.Execute(DataTable) 的说明。

## 例子

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT TOP 50 * FROM Customers ORDER BY Country, CompanyName", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim License
Set License = CreateObject("Aspose.Words.License")
License.SetLicense "C:\MyPath\MyLicense.lic"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")
Dim Doc
Set Doc = Helper.Open("CustomerLabels.doc")

Doc.MailMerge.ExecuteADO RS
Doc.Save "C:\MyPath\CustomerLabels Out VBScript.doc"
```

演示如何使用来自 ADO 数据集的数据运行邮件合并。

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

    // 要使用 ADO 数据集，我们需要添加对 Microsoft ActiveX 数据对象库的引用，
    // 包含在 .NET 发行版中并存储在“adodb.dll”中。
    ADODB.Connection connection = new ADODB.Connection();

    // 创建一个指向“Northwind”数据库文件的连接字符串
    // 在我们的本地文件系统中并打开一个连接。
    string connectionString = @"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=" + DatabaseDir + "Northwind.mdb";
    connection.Open(connectionString);

    // 通过在我们的数据库上运行 SQL 命令来填充我们的数据集。
    // 结果表中的列名需要对应
    // 到将容纳我们的数据的 MERGEFIELDS 的值。
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // 执行邮件合并并保存文档。
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// 创建一个空白文档并使用 MERGEFIELDS 填充它，当执行邮件合并时将接受数据。
/// </summary>
private static Document CreateSourceDocADOMailMerge()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Product:\t");
    builder.InsertField(" MERGEFIELD ProductName");
    builder.Writeln();
    builder.InsertField(" MERGEFIELD QuantityPerUnit");
    builder.Write(" for $");
    builder.InsertField(" MERGEFIELD UnitPrice");

    return doc;
}
```

### 也可以看看

* class [MailMerge](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
