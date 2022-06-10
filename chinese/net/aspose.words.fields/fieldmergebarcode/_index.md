---
title: FieldMergeBarcode
second_title: Aspose.Words for .NET API 参考
description: 实现 MERGEBARCODE 字段
type: docs
weight: 1950
url: /zh/net/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class

实现 MERGEBARCODE 字段。

```csharp
public class FieldMergeBarcode : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldMergeBarcode](fieldmergebarcode)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fieldmergebarcode/addstartstopchar) { get; set; } | 获取或设置是否为条形码类型 NW7 和 CODE39 添加开始/停止字符。 |
| [BackgroundColor](../../aspose.words.fields/fieldmergebarcode/backgroundcolor) { get; set; } | 获取或设置条码符号的背景颜色。有效值范围为 [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fieldmergebarcode/barcodetype) { get; set; } | 获取或设置条码类型（QR等） |
| [BarcodeValue](../../aspose.words.fields/fieldmergebarcode/barcodevalue) { get; set; } | 获取或设置条形码值。 |
| [CaseCodeStyle](../../aspose.words.fields/fieldmergebarcode/casecodestyle) { get; set; } | 获取或设置条码类型 ITF14 的案例代码的样式。有效值为 [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | 获取表示显示字段结果的文本。 |
| [DisplayText](../../aspose.words.fields/fieldmergebarcode/displaytext) { get; set; } | 获取或设置是否将条形码数据（文本）与图像一起显示。 |
| [End](../../aspose.words.fields/field/end) { get; } | 获取表示字段结束的节点。 |
| [ErrorCorrectionLevel](../../aspose.words.fields/fieldmergebarcode/errorcorrectionlevel) { get; set; } | 获取或设置二维码的纠错级别。有效值为 [0, 3]。 |
| [FixCheckDigit](../../aspose.words.fields/fieldmergebarcode/fixcheckdigit) { get; set; } | 获取或设置校验位无效时是否修复。 |
| [ForegroundColor](../../aspose.words.fields/fieldmergebarcode/foregroundcolor) { get; set; } | 获取或设置条码符号的前景色。有效值范围为 [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format) { get; } | 获取[`FieldFormat`](../fieldformat)对象，该对象提供对字段格式的类型化访问。 |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | 获取或设置字段的 LCID。 |
| [PosCodeStyle](../../aspose.words.fields/fieldmergebarcode/poscodestyle) { get; set; } | 获取或设置销售点条形码的样式（条形码类型 UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8）。有效值（不区分大小写）为 [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]。 |
| [Result](../../aspose.words.fields/field/result) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [ScalingFactor](../../aspose.words.fields/fieldmergebarcode/scalingfactor) { get; set; } | 获取或设置符号的比例因子。该值以整数为单位，有效值为 [10, 1000] |
| [Separator](../../aspose.words.fields/field/separator) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [Start](../../aspose.words.fields/field/start) { get; } | 获取表示字段开始的节点。 |
| [SymbolHeight](../../aspose.words.fields/fieldmergebarcode/symbolheight) { get; set; } | 获取或设置符号的高度。单位为 TWIPS（1/1440 英寸）。 |
| [SymbolRotation](../../aspose.words.fields/fieldmergebarcode/symbolrotation) { get; set; } | 获取或设置条码符号的旋转。有效值为 [0, 3] |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包含子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个子 ，则返回其父段落。如果该字段已被删除，则返回 **null** 。 |
| [Unlink](../../aspose.words.fields/field/unlink)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

邮件合并条形码。

### 例子

显示如何对 ITF14 条形码执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 MERGEBARCODE 字段，它将在邮件合并期间接受来自数据源的值。
// 此字段会将合并数据源的“MyQRCode”列中的所有值转换为二维码。
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

// 创建一个 DataTable，其中有一列与我们的 MERGEBARCODE 字段的 BarcodeValue 同名。
// 邮件合并将为每一行创建一个新页面。每个页面将包含一个 DISPLAYBARCODE 字段，
// 这将显示一个二维码，其中包含合并行中的值。
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

显示如何对 CODE39 条形码执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 MERGEBARCODE 字段，它将在邮件合并期间接受来自数据源的值。
// 此字段会将合并数据源的“MyQRCode”列中的所有值转换为二维码。
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

// 创建一个 DataTable，其中有一列与我们的 MERGEBARCODE 字段的 BarcodeValue 同名。
// 邮件合并将为每一行创建一个新页面。每个页面将包含一个 DISPLAYBARCODE 字段，
// 这将显示一个二维码，其中包含合并行中的值。
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

显示如何对 EAN13 条形码执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 MERGEBARCODE 字段，它将在邮件合并期间接受来自数据源的值。
// 此字段会将合并数据源的“MyQRCode”列中的所有值转换为二维码。
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

// 创建一个 DataTable，其中有一列与我们的 MERGEBARCODE 字段的 BarcodeValue 同名。
// 邮件合并将为每一行创建一个新页面。每个页面将包含一个 DISPLAYBARCODE 字段，
// 这将显示一个二维码，其中包含合并行中的值。
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

显示如何在 QR 条形码上执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个 MERGEBARCODE 字段，它将在邮件合并期间接受来自数据源的值。
// 此字段会将合并数据源的“MyQRCode”列中的所有值转换为二维码。
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

// 创建一个 DataTable，其中有一列与我们的 MERGEBARCODE 字段的 BarcodeValue 同名。
// 邮件合并将为每一行创建一个新页面。每个页面将包含一个 DISPLAYBARCODE 字段，
// 这将显示一个二维码，其中包含合并行中的值。
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

* class [Field](../field)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
