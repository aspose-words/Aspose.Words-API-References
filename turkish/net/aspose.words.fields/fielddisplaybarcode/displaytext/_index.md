---
title: FieldDisplayBarcode.DisplayText
second_title: Aspose.Words for .NET API Referansı
description: FieldDisplayBarcode mülk. Resimle birlikte barkod verilerinin metin görüntülenip görüntülenmeyeceğini alır veya ayarlar.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fielddisplaybarcode/displaytext/
---
## FieldDisplayBarcode.DisplayText property

Resimle birlikte barkod verilerinin (metin) görüntülenip görüntülenmeyeceğini alır veya ayarlar.

```csharp
public bool DisplayText { get; set; }
```

### Örnekler

DISPLAYBARCODE alanının nasıl ekleneceğini ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Aşağıda DISPLAYBARCODE alanının görüntüleyebileceği, çeşitli şekillerde dekore edilmiş dört tür barkod bulunmaktadır.
// 1 - Özel renklere sahip QR kodu:
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

// 2 - EAN13 barkodu, rakamlar çubukların altında görüntülenir:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - CODE39 barkodu:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - ITF4 barkodu, belirtilen durum koduyla:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Ayrıca bakınız

* class [FieldDisplayBarcode](../)
* ad alanı [Aspose.Words.Fields](../../fielddisplaybarcode/)
* toplantı [Aspose.Words](../../../)


