---
title: FieldMergeBarcode.ErrorCorrectionLevel
linktitle: ErrorCorrectionLevel
articleTitle: ErrorCorrectionLevel
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldMergeBarcode ErrorCorrectionLevel para optimizar la fiabilidad de su código QR. Configure valores de 0 a 3 para una mejor corrección de errores.
type: docs
weight: 80
url: /es/net/aspose.words.fields/fieldmergebarcode/errorcorrectionlevel/
---
## FieldMergeBarcode.ErrorCorrectionLevel property

Obtiene o establece el nivel de corrección de errores del código QR. Los valores válidos son [0, 3].

```csharp
public string ErrorCorrectionLevel { get; set; }
```

## Ejemplos

Muestra cómo realizar una combinación de correspondencia en códigos de barras QR.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo MERGEBARCODE, que aceptará valores de una fuente de datos durante una combinación de correspondencia.
// Este campo convertirá todos los valores de la columna "MyQRCode" de una fuente de datos combinada en códigos QR.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Aplicar colores y escala personalizados.
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

// Cree una DataTable con una columna con el mismo nombre que el BarcodeValue de nuestro campo MERGEBARCODE.
La combinación de correspondencia creará una página nueva para cada fila. Cada página contendrá un campo DISPLAYBARCODE.
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
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
