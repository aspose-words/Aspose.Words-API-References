---
title: FieldMergeBarcode.CaseCodeStyle
linktitle: CaseCodeStyle
articleTitle: CaseCodeStyle
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldMergeBarcode CaseCodeStyle para códigos de barras ITF14. Personalice fácilmente el estilo de su código de caso con opciones válidas como STDEXTADD.
type: docs
weight: 60
url: /es/net/aspose.words.fields/fieldmergebarcode/casecodestyle/
---
## FieldMergeBarcode.CaseCodeStyle property

Obtiene o establece el estilo de un código de caso para el tipo de código de barras ITF14. Los valores válidos son [STD&#x7C;EXT&#x7C;ADD]

```csharp
public string CaseCodeStyle { get; set; }
```

## Ejemplos

Muestra cómo realizar una combinación de correspondencia en códigos de barras ITF14.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un campo MERGEBARCODE, que aceptará valores de una fuente de datos durante una combinación de correspondencia.
// Este campo convertirá todos los valores de la columna "MyITF14Barcode" de una fuente de datos combinada en códigos de barras ITF14.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// Cree una DataTable con una columna con el mismo nombre que el BarcodeValue de nuestro campo MERGEBARCODE.
La combinación de correspondencia creará una página nueva para cada fila. Cada página contendrá un campo DISPLAYBARCODE.
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

### Ver también

* class [FieldMergeBarcode](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
