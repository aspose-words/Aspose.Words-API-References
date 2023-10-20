---
title: FieldSkipIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: 用于 .NET 的 Aspose.Words
description: FieldSkipIf RightExpression 财产. 获取或设置比较表达式的右侧部分 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldskipif/rightexpression/
---
## FieldSkipIf.RightExpression property

获取或设置比较表达式的右侧部分。

```csharp
public string RightExpression { get; set; }
```

## 例子

演示如何使用 SKIPIF 字段在邮件合并中跳过页面。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入 SKIPIF 字段。如果邮件合并操作的当前行满足条件
// 该字段的表达式表示该状态，则邮件合并操作将中止当前行，
// 丢弃当前合并文档，然后立即移动到下一行以开始下一个合并文档。
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// 将构建器移至 SKIPIF 字段的分隔符，以便我们可以在 SKIPIF 字段内放置 MERGEFIELD。
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD 引用数据表中的“部门”列。如果该表中的一行
// 在其“部门”列中值为“HR”，则该行将满足条件。
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// 将内容添加到我们的文档中，创建数据源，并执行邮件合并。
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // 该表有三行，其中一行满足 SKIPIF 字段的条件。
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

演示如何使用 MERGEREC 和 MERGESEQ 字段对邮件合并输出文档中的邮件合并记录进行编号和计数。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// MERGEREC 字段将打印每个合并输出文档中正在合并的数据的行号。
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// MERGESEQ 字段将计算成功合并的数量并在每个页面上打印当前值。
// 如果邮件合并不跳过任何行并且不调用 SKIP/SKIPIF/NEXT/NEXTIF 字段，则所有合并都会成功。
// MERGESEQ 和 MERGEREC 字段将显示相同的结果，表明它们的邮件合并成功。
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// 插入一个 SKIPIF 字段，如果名称是“John Doe”，该字段将跳过合并。
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// 创建一个包含 3 行的数据源，其中一行将“John Doe”作为“Name”列的值。
// 由于 SKIPIF 字段将被该值触发一次，因此邮件合并的输出将有 2 页而不是 3 页。
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

* class [FieldSkipIf](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
