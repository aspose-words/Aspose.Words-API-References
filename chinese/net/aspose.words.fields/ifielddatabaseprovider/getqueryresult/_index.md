---
title: IFieldDatabaseProvider.GetQueryResult
linktitle: GetQueryResult
articleTitle: GetQueryResult
second_title: Aspose.Words for .NET
description: 探索 IFieldDatabaseProvider 的 GetQueryResult 方法，实现高效的数据检索。立即简化您的查询并提升数据库性能！
type: docs
weight: 10
url: /zh/net/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider.GetQueryResult method

返回查询结果。

```csharp
public FieldDatabaseDataTable GetQueryResult(string fileName, string connection, string query, 
    FieldDatabase field)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | \d 字段开关中指定的数据库的完整路径和文件名。 |
| connection | String | 与 \c 字段开关中指定的数据的连接。 |
| query | String | 查询 \s 字段开关中指定的数据库的 SQL 指令集。 |
| field | FieldDatabase | 正在更新的字段。 |

### 返回值

这[`FieldDatabaseDataTable`](../../fielddatabasedatatable/)应该用于字段更新的实例。

## 例子

展示如何从数据库中提取数据并将其作为字段插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 此 DATABASE 字段将在数据库上运行查询，并在表中显示结果。
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// 插入另一个数据库字段，其中包含更复杂的查询，该查询按总销售额降序对所有产品进行排序。
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// 这些属性具有与 LIMIT 和 TOP 子句相同的功能。
// 配置它们以仅显示字段表中查询结果的第 1 至 10 行。
field.FirstRecord = "1";
field.LastRecord = "10";

// 此属性是我们要用于表格的格式的索引。表格格式列表位于“表格自动套用格式...”菜单中
// 在 Microsoft Word 中创建数据库字段时显示的内容。索引 #10 对应于“Colorful 3”格式。
field.TableFormat = "10";

// FormatAttribute 属性是存储多个标志的整数的字符串表示形式。
// 我们可以通过在此属性中设置不同的标志来分别应用 TableFormat 属性指向的格式。
// 我们使用的数字是与表格样式的不同方面相对应的值的组合的总和。
// 63 代表 1（边框）+ 2（阴影）+ 4（字体）+ 8（颜色）+ 16（自动调整）+ 32（标题行）。
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### 也可以看看

* class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* class [FieldDatabase](../../fielddatabase/)
* interface [IFieldDatabaseProvider](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
