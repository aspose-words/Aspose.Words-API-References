---
title: FieldDisplayBarcode
second_title: Aspose.Words for .NET API 参考
description: 实现 DISPLAYBARCODE 字段
type: docs
weight: 1610
url: /zh/net/aspose.words.fields/fielddisplaybarcode/
---
## FieldDisplayBarcode class

实现 DISPLAYBARCODE 字段。

```csharp
public class FieldDisplayBarcode : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldDisplayBarcode](fielddisplaybarcode)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fielddisplaybarcode/addstartstopchar) { get; set; } | 获取或设置是否为条形码类型 NW7 和 CODE39 添加开始/停止字符。 |
| [BackgroundColor](../../aspose.words.fields/fielddisplaybarcode/backgroundcolor) { get; set; } | 获取或设置条码符号的背景颜色。有效值范围为 [0, 0xFFFFFF] |
| [BarcodeType](../../aspose.words.fields/fielddisplaybarcode/barcodetype) { get; set; } | 获取或设置条码类型（QR等） |
| [BarcodeValue](../../aspose.words.fields/fielddisplaybarcode/barcodevalue) { get; set; } | 获取或设置条形码值。 |
| [CaseCodeStyle](../../aspose.words.fields/fielddisplaybarcode/casecodestyle) { get; set; } | 获取或设置条码类型 ITF14 的案例代码的样式。有效值为 [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | 获取表示显示字段结果的文本。 |
| [DisplayText](../../aspose.words.fields/fielddisplaybarcode/displaytext) { get; set; } | 获取或设置是否将条形码数据（文本）与图像一起显示。 |
| [End](../../aspose.words.fields/field/end) { get; } | 获取表示字段结束的节点。 |
| [ErrorCorrectionLevel](../../aspose.words.fields/fielddisplaybarcode/errorcorrectionlevel) { get; set; } | 获取或设置二维码的纠错级别。有效值为 [0, 3]。 |
| [FixCheckDigit](../../aspose.words.fields/fielddisplaybarcode/fixcheckdigit) { get; set; } | 获取或设置校验位无效时是否修复。 |
| [ForegroundColor](../../aspose.words.fields/fielddisplaybarcode/foregroundcolor) { get; set; } | 获取或设置条码符号的前景色。有效值范围为 [0, 0xFFFFFF] |
| [Format](../../aspose.words.fields/field/format) { get; } | 获取[`FieldFormat`](../fieldformat)对象，该对象提供对字段格式的类型化访问。 |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | 获取或设置字段的 LCID。 |
| [PosCodeStyle](../../aspose.words.fields/fielddisplaybarcode/poscodestyle) { get; set; } | 获取或设置销售点条形码的样式（条形码类型 UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8）。有效值（不区分大小写）为 [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]。 |
| [Result](../../aspose.words.fields/field/result) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [ScalingFactor](../../aspose.words.fields/fielddisplaybarcode/scalingfactor) { get; set; } | 获取或设置符号的比例因子。该值以整数为单位，有效值为 [10, 1000] |
| [Separator](../../aspose.words.fields/field/separator) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [Start](../../aspose.words.fields/field/start) { get; } | 获取表示字段开始的节点。 |
| [SymbolHeight](../../aspose.words.fields/fielddisplaybarcode/symbolheight) { get; set; } | 获取或设置符号的高度。单位为 TWIPS（1/1440 英寸）。 |
| [SymbolRotation](../../aspose.words.fields/fielddisplaybarcode/symbolrotation) { get; set; } | 获取或设置条码符号的旋转。有效值为 [0, 3] |
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

插入条形码。

### 例子

显示如何在 QR 条形码上执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// 以下是 DISPLAYBARCODE 字段可以显示的四种类型的条码，以各种方式装饰。
// 1 - 带有自定义颜色的二维码：
field.BarcodeType = "QR";
field.BarcodeValue = "ABC123";
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field.GetFieldCode());
builder.Writeln();

// 2 - EAN13 条码，条码下方显示数字：
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - CODE39 条形码：
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - ITF4 条形码，带有指定的案例代码：
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

显示如何插入 DISPLAYBARCODE 字段并设置其属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// 以下是 DISPLAYBARCODE 字段可以显示的四种类型的条码，以各种方式装饰。
// 1 - 带有自定义颜色的二维码：
field.BarcodeType = "QR";
field.BarcodeValue = "ABC123";
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(" DISPLAYBARCODE  ABC123 QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0", field.GetFieldCode());
builder.Writeln();

// 2 - EAN13 条码，条码下方显示数字：
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - CODE39 条形码：
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - ITF4 条形码，带有指定的案例代码：
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### 也可以看看

* class [Field](../field)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
