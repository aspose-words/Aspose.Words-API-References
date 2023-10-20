---
title: FieldMergeBarcode.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: 用于 .NET 的 Aspose.Words
description: FieldMergeBarcode DisplayText 财产. 获取或设置是否与图像一起显示条形码数据文本 在 C#.
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

演示如何对 EAN13 条形码执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个MERGEBARCODE 字段，该字段将在邮件合并期间接受来自数据源的值。
// 此字段会将合并数据源的“MyEAN13Barcode”列中的所有值转换为 EAN13 条形码。
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// 在条形下方显示条形码的数值。
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 创建一个 DataTable，其中有一列与我们的MERGEBARCODE字段的BarcodeValue同名。
// 邮件合并将为每一行创建一个新页面。每个页面都会包含一个 DISPLAYBARCODE 字段，
// 这将显示 EAN13 条形码以及合并行中的值。
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
