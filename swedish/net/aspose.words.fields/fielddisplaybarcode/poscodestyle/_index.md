---
title: PosCodeStyle
second_title: Aspose.Words för .NET API Referens
description: Hämtar eller ställer in stilen för en streckkod för försäljningsställen streckkodstyperna UPCAx7CUPCEx7CEAN13x7CEAN8. De giltiga värdena okänsliga skiftlägen är STDx7CSUP2x7CSUP5x7CCASE.
type: docs
weight: 110
url: /sv/net/aspose.words.fields/fielddisplaybarcode/poscodestyle/
---
## FieldDisplayBarcode.PosCodeStyle property

Hämtar eller ställer in stilen för en streckkod för försäljningsställen (streckkodstyperna UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). De giltiga värdena (okänsliga skiftlägen) är [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

### Exempel

Visar hur man infogar ett DISPLAYBARCODE-fält och ställer in dess egenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Nedan finns fyra typer av streckkoder, dekorerade på olika sätt, som fältet DISPLAYBARCODE kan visa.
// 1 - QR-kod med anpassade färger:
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

// 2 - EAN13 streckkod, med siffrorna under strecken:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - CODE39 streckkod:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - ITF4 streckkod, med en specificerad fallkod:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Se även

* class [FieldDisplayBarcode](../../fielddisplaybarcode)
* namnutrymme [Aspose.Words.Fields](../../fielddisplaybarcode)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->