---
title: FieldMergeBarcode.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words for .NET
description: 使用 FieldMergeBarcode 的 DisplayText 属性控制条形码文本的显示。轻松增强应用程序的可读性和功能性。
type: docs
weight: 70
url: /zh/net/aspose.words.fields/fieldmergebarcode/displaytext/
---
## FieldMergeBarcode.DisplayText property

获取或设置是否与图像一起显示条形码数据（文本）。

```csharp
public bool DisplayText { get; set; }
```

## 例子

展示如何对 EAN13 条形码执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 MERGEBARCODE 字段，它将在邮件合并期间接受来自数据源的值。
// 此字段将合并数据源的“MyEAN13Barcode”列中的所有值转换为 EAN13 条形码。
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// 显示条形码下方的条形码的数值。
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 创建一个 DataTable，其列名与我们的 MERGEBARCODE 字段的 BarcodeValue 相同。
// 邮件合并将为每一行创建一个新页面。每页将包含一个 DISPLAYBARCODE 字段，
// 将显示带有合并行值的 EAN13 条形码。
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

### 也可以看看

* class [FieldMergeBarcode](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
