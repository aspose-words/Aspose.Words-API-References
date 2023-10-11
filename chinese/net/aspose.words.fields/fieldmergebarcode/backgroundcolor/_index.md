---
title: FieldMergeBarcode.BackgroundColor
second_title: Aspose.Words for .NET API 参考
description: FieldMergeBarcode 财产. 获取或设置条形码符号的背景颜色有效值范围为 0 0xFFFFFF
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldmergebarcode/backgroundcolor/
---
## FieldMergeBarcode.BackgroundColor property

获取或设置条形码符号的背景颜色。有效值范围为 [0, 0xFFFFFF]

```csharp
public string BackgroundColor { get; set; }
```

### 例子

演示如何对 QR 条形码执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个MERGEBARCODE 字段，该字段将在邮件合并期间接受来自数据源的值。
// 该字段会将合并数据源的“MyQRCode”列中的所有值转换为二维码。
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// 应用自定义颜色和缩放。
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// 创建一个 DataTable，其中有一列与我们的MERGEBARCODE字段的BarcodeValue同名。
// 邮件合并将为每一行创建一个新页面。每个页面都会包含一个 DISPLAYBARCODE 字段，
// 这将显示带有合并行中的值的二维码。
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

### 也可以看看

* class [FieldMergeBarcode](../)
* 命名空间 [Aspose.Words.Fields](../../fieldmergebarcode/)
* 部件 [Aspose.Words](../../../)


