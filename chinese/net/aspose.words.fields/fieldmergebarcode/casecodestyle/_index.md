---
title: FieldMergeBarcode.CaseCodeStyle
linktitle: CaseCodeStyle
articleTitle: CaseCodeStyle
second_title: Aspose.Words for .NET
description: 探索 ITF14 条形码的 FieldMergeBarcode CaseCodeStyle 属性。使用 STDEXTADD 等有效选项轻松自定义 Case Code 样式。
type: docs
weight: 60
url: /zh/net/aspose.words.fields/fieldmergebarcode/casecodestyle/
---
## FieldMergeBarcode.CaseCodeStyle property

获取或设置 ITF14 条形码类型的 Case Code 样式。有效值为 [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

## 例子

展示如何对 ITF14 条形码执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 MERGEBARCODE 字段，它将在邮件合并期间接受来自数据源的值。
// 此字段将合并数据源的“MyITF14Barcode”列中的所有值转换为 ITF14 条形码。
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// 创建一个 DataTable，其列名与我们的 MERGEBARCODE 字段的 BarcodeValue 相同。
// 邮件合并将为每一行创建一个新页面。每页将包含一个 DISPLAYBARCODE 字段，
// 将显示一个带有合并行值的 ITF14 条形码。
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

### 也可以看看

* class [FieldMergeBarcode](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
