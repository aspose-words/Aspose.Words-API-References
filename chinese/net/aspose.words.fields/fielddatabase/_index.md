---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldDatabase 类，高效实现文档中的数据库字段。立即增强您的文档自动化！
type: docs
weight: 2150
url: /zh/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

实现数据库字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldDatabase : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldDatabase](fielddatabase/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | 获取或设置与数据的连接。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | 获取或设置数据库的完整路径和文件名 |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | 获取或设置要插入的第一个数据记录的整数记录号。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | 获取或设置要应用于表的格式属性。 |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | 获取或设置是否将数据库中的字段名称作为列标题插入到结果表中。 |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | 获取或设置是否在合并开始时插入数据。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | 获取或设置要插入的最后一条数据记录的整数记录号。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | 获取或设置一组查询数据库的 SQL 指令。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | 获取或设置应用于数据库查询结果的格式。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

将数据库查询的结果插入到 WordprocessingML 表中。

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

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
