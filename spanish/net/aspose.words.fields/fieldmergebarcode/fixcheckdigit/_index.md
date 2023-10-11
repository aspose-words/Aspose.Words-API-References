---
title: FieldMergeBarcode.FixCheckDigit
second_title: Referencia de API de Aspose.Words para .NET
description: FieldMergeBarcode propiedad. Obtiene o establece si se corrige el dígito de control si no es válido.
type: docs
weight: 90
url: /es/net/aspose.words.fields/fieldmergebarcode/fixcheckdigit/
---
## FieldMergeBarcode.FixCheckDigit property

Obtiene o establece si se corrige el dígito de control si no es válido.

```csharp
public bool FixCheckDigit { get; set; }
```

### Ejemplos

Muestra cómo realizar una combinación de correspondencia en códigos de barras EAN13.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo MERGEBARCODE, que aceptará valores de una fuente de datos durante una combinación de correspondencia.
// Este campo convertirá todos los valores en la columna "MyEAN13Barcode" de una fuente de datos combinada en códigos de barras EAN13.
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

// Crea una DataTable con una columna con el mismo nombre que BarcodeValue de nuestro campo MERGEBARCODE.
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

### Ver también

* class [FieldMergeBarcode](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldmergebarcode/)
* asamblea [Aspose.Words](../../../)


