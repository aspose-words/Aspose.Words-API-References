---
title: FieldMergeBarcode.AddStartStopChar
linktitle: AddStartStopChar
articleTitle: AddStartStopChar
second_title: Aspose.Words para .NET
description: FieldMergeBarcode AddStartStopChar propiedad. Obtiene o establece si se deben agregar caracteres de inicio/parada para los tipos de códigos de barras NW7 y CODE39 en C#.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldmergebarcode/addstartstopchar/
---
## FieldMergeBarcode.AddStartStopChar property

Obtiene o establece si se deben agregar caracteres de inicio/parada para los tipos de códigos de barras NW7 y CODE39.

```csharp
public bool AddStartStopChar { get; set; }
```

## Ejemplos

Muestra cómo realizar una combinación de correspondencia en códigos de barras CODE39.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo MERGEBARCODE, que aceptará valores de una fuente de datos durante una combinación de correspondencia.
// Este campo convertirá todos los valores de la columna "MyCODE39Barcode" de una fuente de datos combinada en códigos de barras CODE39.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Edita su apariencia para mostrar caracteres de inicio/parada.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// Crea una DataTable con una columna con el mismo nombre que BarcodeValue de nuestro campo MERGEBARCODE.
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

### Ver también

* class [FieldMergeBarcode](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
