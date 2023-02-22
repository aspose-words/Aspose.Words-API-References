---
title: Class FieldSkipIf
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.FieldSkipIf 班级. 实现 SKIPIF 字段
type: docs
weight: 2270
url: /zh/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

实现 SKIPIF 字段。

```csharp
public class FieldSkipIf : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldSkipIf](fieldskipif/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldskipif/comparisonoperator/) { get; set; } | 获取或设置比较运算符。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段end的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 得到一个[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | 获取或设置比较表达式的左边部分。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | 获取或设置比较表达式的右边部分。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（或字段结束，如果没有分隔符）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回 **无效的**. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update/)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

比较表达式指定的值[`LeftExpression`](./leftexpression/)和[`RightExpression`](./rightexpression/) 使用指定的运算符进行比较[`ComparisonOperator`](./comparisonoperator/).如果比较为真，则SKIPIF 取消当前合并文档，移动到数据源中的下一条数据记录，并开始新的合并文档。 如果比较为假，则继续当前合并文档。

### 例子

显示如何使用 SKIPIF 字段跳过邮件合并中的页面。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 SKIPIF 字段。如果邮件合并操作的当前行满足条件
// 该字段的表达式状态，然后邮件合并操作中止当前行，
// 丢弃当前的合并文档，然后立即移动到下一行开始下一个合并文档。
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// 将构建器移动到 SKIPIF 字段的分隔符处，以便我们可以在 SKIPIF 字段内放置一个 MERGEFIELD。
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD 指的是我们数据表中的“部门”列。如果该表中的一行
// 在其“部门”列中的值为“HR”，则该行将满足条件。
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// 向我们的文档添加内容，创建数据源，执行邮件合并。
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // 这个表有三行，其中一行满足我们的 SKIPIF 字段的条件。
// 邮件合并将产生两个页面。
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

演示如何使用 MERGEREC 和 MERGESEQ 字段来对邮件合并的输出文档中的邮件合并记录进行编号和计数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// MERGEREC 字段将打印每个合并输出文档中要合并的数据的行号。
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// MERGESEQ 字段将计算成功合并的次数并在每个相应的页面上打印当前值。
// 如果邮件合并没有跳过任何行并且没有调用 SKIP/SKIPIF/NEXT/NEXTIF 字段，则所有合并都成功。
// MERGESEQ 和 MERGEREC 字段将显示它们的邮件合并成功的相同结果。
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// 插入一个 SKIPIF 字段，如果名称是“John Doe”，它将跳过合并。
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// 创建一个包含 3 行的数据源，其中一行将“John Doe”作为“Name”列的值。
// 因为 SKIPIF 字段将被该值触发一次，所以我们的邮件合并的输出将有 2 页而不是 3 页。
// 在第 1 页上，MERGESEQ 和 MERGEREC 字段都将显示“1”。
// 在第 2 页上，MERGEREC 字段将显示“3”，MERGESEQ 字段将显示“2”。
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


