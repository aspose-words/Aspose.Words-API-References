---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: Aspose.Words for .NET
description: 使用 MailMerge ExecuteADO 方法简化文档创建。轻松合并 ADO 记录集数据，实现高效、个性化的输出。
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

当您打算从非托管代码（例如使用 ASP 或 Visual Basic 6.0 构建的应用程序）中使用 Aspose.Words 类作为 COM 对象时，此方法很有用。

此方法忽略RemoveUnusedRegions选项。

有关详细信息，请参阅[`Execute`](../execute/)。

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

展示如何使用 ADO 数据集中的数据运行邮件合并。

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // 执行邮件合并并保存文档。
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// 创建一个空白文档并用 MERGEFIELDS 填充它，当执行邮件合并时它将接受数据。
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
