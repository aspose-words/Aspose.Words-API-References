---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: 用于 .NET 的 Aspose.Words
description: MailMerge ExecuteADO 方法. 将 ADO Recordset 对象的邮件合并到文档中 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

将 ADO Recordset 对象的邮件合并到文档中。

```csharp
public void ExecuteADO(object recordset)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| recordset | Object | ADO 记录集或记录对象。 |

## 评论

当您打算使用非托管代码中的 Aspose.Words 类 as COM 对象（例如使用 ASP 或 Visual Basic 6.0 构建的应用程序）时，此方法非常有用。

该方法忽略了RemoveUnusedRegions选项。

欲了解更多信息，请参阅描述[`Execute`](../execute/)。

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

演示如何使用 ADO 数据集中的数据运行邮件合并。

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // 执行邮件合并并保存文档。
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// 创建一个空白文档并用 MERGEFIELDS 填充它，该 MERGEFIELDS 将在执行邮件合并时接受数据。
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
