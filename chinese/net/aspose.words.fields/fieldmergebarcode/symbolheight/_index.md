---
title: FieldMergeBarcode.SymbolHeight
linktitle: SymbolHeight
articleTitle: SymbolHeight
second_title: Aspose.Words for .NET
description: 调整 FieldMergeBarcode 的 SymbolHeight 属性，以 TWIPS 为单位自定义条形码的高度。精准提升数据呈现效果！
type: docs
weight: 130
url: /zh/net/aspose.words.fields/fieldmergebarcode/symbolheight/
---
## FieldMergeBarcode.SymbolHeight property

获取或设置符号的高度。单位为TWIPS（1/1440英寸）。

```csharp
public string SymbolHeight { get; set; }
```

## 例子

展示如何对二维码执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 MERGEBARCODE 字段，它将在邮件合并期间接受来自数据源的值。
// 此字段将合并数据源的“MyQRCode”列中的所有值转换为二维码。
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// 应用自定义颜色和缩放比例。
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

// 创建一个 DataTable，其列名与我们的 MERGEBARCODE 字段的 BarcodeValue 相同。
// 邮件合并将为每一行创建一个新页面。每页将包含一个 DISPLAYBARCODE 字段，
// 将显示一个带有合并行值的二维码。
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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
