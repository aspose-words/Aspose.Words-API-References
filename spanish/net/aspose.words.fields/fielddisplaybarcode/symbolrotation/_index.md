---
title: FieldDisplayBarcode.SymbolRotation
linktitle: SymbolRotation
articleTitle: SymbolRotation
second_title: Aspose.Words para .NET
description: Descubra la propiedad SymbolRotation de FieldDisplayBarcode. Ajuste fácilmente la rotación del código de barras para una lectura óptima con valores válidos de 0 a 3. ¡Mejore la visualización de sus datos!
type: docs
weight: 140
url: /es/net/aspose.words.fields/fielddisplaybarcode/symbolrotation/
---
## FieldDisplayBarcode.SymbolRotation property

Obtiene o establece la rotación del símbolo del código de barras. Los valores válidos son [0, 3]

```csharp
public string SymbolRotation { get; set; }
```

## Ejemplos

Muestra cómo insertar un campo DISPLAYBARCODE y configurar sus propiedades.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDisplayBarcode field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);

// A continuación se muestran cuatro tipos de códigos de barras, decorados de diversas maneras, que el campo DISPLAYBARCODE puede mostrar.
// 1 - Código QR con colores personalizados:
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

// 2 - Código de barras EAN13, con los dígitos mostrados debajo de las barras:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "501234567890";
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(" DISPLAYBARCODE  501234567890 EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// 3 - Código de barras CODE39:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "12345ABCDE";
field.AddStartStopChar = true;

Assert.AreEqual(" DISPLAYBARCODE  12345ABCDE CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// 4 - Código de barras ITF4, con un código de caso especificado:
field = (FieldDisplayBarcode)builder.InsertField(FieldType.FieldDisplayBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "09312345678907";
field.CaseCodeStyle = "STD";

Assert.AreEqual(" DISPLAYBARCODE  09312345678907 ITF14 \\c STD", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.DISPLAYBARCODE.docx");
```

### Ver también

* class [FieldDisplayBarcode](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
