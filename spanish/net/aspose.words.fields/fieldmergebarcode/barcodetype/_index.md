---
title: BarcodeType
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece el tipo de código de barras QR etc.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldmergebarcode/barcodetype/
---
## FieldMergeBarcode.BarcodeType property

Obtiene o establece el tipo de código de barras (QR, etc.)

```csharp
public string BarcodeType { get; set; }
```

### Ejemplos

Muestra cómo realizar una combinación de correspondencia en códigos de barras ITF14.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo MERGEBARCODE, que aceptará valores de una fuente de datos durante una combinación de correspondencia.
// Este campo convertirá todos los valores en la columna "MyITF14Barcode" de una fuente de datos combinados en códigos de barras ITF14.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// Crear un DataTable con una columna con el mismo nombre que el BarcodeValue de nuestro campo MERGEBARCODE.
// La combinación de correspondencia creará una nueva página para cada fila. Cada página contendrá un campo DISPLAYBARCODE,
// que mostrará un código de barras ITF14 con el valor de la fila fusionada.
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

Muestra cómo realizar una combinación de correspondencia en códigos de barras CODE39.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo MERGEBARCODE, que aceptará valores de una fuente de datos durante una combinación de correspondencia.
// Este campo convertirá todos los valores en la columna "MyCODE39Barcode" de una fuente de datos combinados en códigos de barras CODE39.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Edite su apariencia para mostrar los caracteres de inicio/finalización.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// Crear un DataTable con una columna con el mismo nombre que el BarcodeValue de nuestro campo MERGEBARCODE.
// La combinación de correspondencia creará una nueva página para cada fila. Cada página contendrá un campo DISPLAYBARCODE,
// que mostrará un código de barras CODE39 con el valor de la fila fusionada.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

Muestra cómo realizar una combinación de correspondencia en códigos de barras EAN13.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo MERGEBARCODE, que aceptará valores de una fuente de datos durante una combinación de correspondencia.
// Este campo convertirá todos los valores en la columna "MyEAN13Barcode" de una fuente de datos combinados en códigos de barras EAN13.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Muestra el valor numérico del código de barras debajo de las barras.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// Crear un DataTable con una columna con el mismo nombre que el BarcodeValue de nuestro campo MERGEBARCODE.
// La combinación de correspondencia creará una nueva página para cada fila. Cada página contendrá un campo DISPLAYBARCODE,
// que mostrará un código de barras EAN13 con el valor de la fila fusionada.
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

Muestra cómo realizar una combinación de correspondencia en códigos de barras QR.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo MERGEBARCODE, que aceptará valores de una fuente de datos durante una combinación de correspondencia.
// Este campo convertirá todos los valores en la columna "MyQRCode" de una fuente de datos combinados en códigos QR.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Aplicar colores y escalas personalizados.
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

// Crear un DataTable con una columna con el mismo nombre que el BarcodeValue de nuestro campo MERGEBARCODE.
// La combinación de correspondencia creará una nueva página para cada fila. Cada página contendrá un campo DISPLAYBARCODE,
// que mostrará un código QR con el valor de la fila fusionada.
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

### Ver también

* class [FieldMergeBarcode](../../fieldmergebarcode)
* espacio de nombres [Aspose.Words.Fields](../../fieldmergebarcode)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
