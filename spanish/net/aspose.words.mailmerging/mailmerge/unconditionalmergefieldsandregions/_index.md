---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad UnconditionalMergeFieldsAndRegions de MailMerge mejora la automatización de documentos al fusionar campos y regiones sin límites condicionales.
type: docs
weight: 140
url: /es/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Obtiene o establece un valor que indica si los campos de fusión y las regiones de fusión se fusionan independientemente de la condición del campo IF principal.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` .

## Ejemplos

Muestra cómo fusionar campos o regiones independientemente de la condición del campo IF principal.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un MERGEFIELD anidado dentro de un campo IF.
// Dado que la declaración del campo SI es falsa, no se mostrará el resultado de MERGEFIELD.
// MERGEFIELD tampoco recibirá ningún dato durante una combinación de correspondencia.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Si establecemos el indicador "UnconditionalMergeFieldsAndRegions" en "verdadero",
// Nuestra combinación de correspondencia insertará datos en campos no mostrados, como nuestro MERGEFIELD y todos los demás.
// Si establecemos el indicador "UnconditionalMergeFieldsAndRegions" en "falso",
// nuestra combinación de correspondencia no insertará datos en MERGEFIELDs ocultos por campos IF con declaraciones falsas.
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
