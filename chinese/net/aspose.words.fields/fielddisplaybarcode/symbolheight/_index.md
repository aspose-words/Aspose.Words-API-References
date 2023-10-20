---
title: FieldDisplayBarcode.SymbolHeight
linktitle: SymbolHeight
articleTitle: SymbolHeight
second_title: 用于 .NET 的 Aspose.Words
description: FieldDisplayBarcode SymbolHeight 财产. 获取或设置符号的高度单位为 TWIPS1/1440 英寸 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words.fields/fielddisplaybarcode/symbolheight/
---
## FieldDisplayBarcode.SymbolHeight property

获取或设置符号的高度。单位为 TWIPS（1/1440 英寸）。

```csharp
public string SymbolHeight { get; set; }
```

## 例子

演示如何插入 DISPLAYBARCODE 字段并设置其属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// 下面是 DISPLAYBARCODE 字段可以显示的四种类型的条形码，以各种方式装饰。
// 1 - 具有自定义颜色的 QR 码：
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

// 2 - EAN13 条形码，数字显示在条形下方：
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

// 4 - ITF4 条形码，具有指定的案例代码：
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### 也可以看看

* class [FieldDisplayBarcode](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
