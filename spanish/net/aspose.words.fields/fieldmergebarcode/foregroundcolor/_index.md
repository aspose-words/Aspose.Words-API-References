---
title: FieldMergeBarcode.ForegroundColor
second_title: Referencia de API de Aspose.Words para .NET
description: FieldMergeBarcode propiedad. Obtiene o establece el color de primer plano del símbolo del código de barras. Los valores válidos están en el rango 0 0xFFFFFF
type: docs
weight: 100
url: /es/net/aspose.words.fields/fieldmergebarcode/foregroundcolor/
---
## FieldMergeBarcode.ForegroundColor property

Obtiene o establece el color de primer plano del símbolo del código de barras. Los valores válidos están en el rango [0, 0xFFFFFF]

```csharp
public string ForegroundColor { get; set; }
```

### Ejemplos

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

* class [FieldMergeBarcode](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldmergebarcode/)
* asamblea [Aspose.Words](../../../)


