---
title: FieldDisplayBarcode.SymbolHeight
second_title: Aspose.Words per .NET API Reference
description: FieldDisplayBarcode proprietà. Ottiene o imposta laltezza del simbolo. Le unità sono in TWIPS 1/1440 di pollice.
type: docs
weight: 130
url: /it/net/aspose.words.fields/fielddisplaybarcode/symbolheight/
---
## FieldDisplayBarcode.SymbolHeight property

Ottiene o imposta l'altezza del simbolo. Le unità sono in TWIPS (1/1440 di pollice).

```csharp
public string SymbolHeight { get; set; }
```

### Esempi

Mostra come inserire un campo DISPLAYBarCODE e impostarne le proprietà.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// Di seguito sono riportati quattro tipi di codici a barre, decorati in vari modi, che il campo DISPLAYBARCODE può visualizzare.
// 1 - Codice QR con colori personalizzati:
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

// 2 - Codice a barre EAN13, con le cifre visualizzate sotto le barre:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - Codice a barre CODE39:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - Codice a barre ITF4, con un codice caso specificato:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Guarda anche

* class [FieldDisplayBarcode](../)
* spazio dei nomi [Aspose.Words.Fields](../../fielddisplaybarcode/)
* assemblea [Aspose.Words](../../../)


