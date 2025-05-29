---
title: FieldDisplayBarcode.ErrorCorrectionLevel
linktitle: ErrorCorrectionLevel
articleTitle: ErrorCorrectionLevel
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldDisplayBarcode ErrorCorrectionLevel для QR-кодов. Легко управляйте уровнями исправления ошибок с допустимыми параметрами от 0 до 3.
type: docs
weight: 80
url: /ru/net/aspose.words.fields/fielddisplaybarcode/errorcorrectionlevel/
---
## FieldDisplayBarcode.ErrorCorrectionLevel property

Получает или задает уровень исправления ошибок QR-кода. Допустимые значения: [0, 3].

```csharp
public string ErrorCorrectionLevel { get; set; }
```

## Примеры

Показывает, как вставить поле DISPLAYBARCODE и задать его свойства.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Ниже приведены четыре типа штрих-кодов, оформленных различными способами, которые может отображать поле DISPLAYBARCODE.
// 1 - QR-код с пользовательскими цветами:
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

// 2 - штрих-код EAN13, в котором цифры отображаются под штрихами:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - штрих-код CODE39:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - штрих-код ITF4, с указанным кодом корпуса:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Смотрите также

* class [FieldDisplayBarcode](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
