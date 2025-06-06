---
title: MailMerge.PreserveUnusedTags
linktitle: PreserveUnusedTags
articleTitle: PreserveUnusedTags
second_title: Aspose.Words para .NET
description: Descubra la propiedad PreserveUnusedTags de MailMerge para administrar de manera efectiva las etiquetas mustache no utilizadas y mejorar su proceso de automatización de documentos.
type: docs
weight: 80
url: /es/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

Obtiene o establece un valor que indica si se deben conservar las etiquetas "bigote" no utilizadas.

```csharp
public bool PreserveUnusedTags { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` .

## Ejemplos

Muestra cómo conservar la apariencia de las etiquetas de combinación de correspondencia alternativas que no se utilizan durante una combinación de correspondencia.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // De manera predeterminada, una combinación de correspondencia coloca datos de cada fila de una tabla en MERGEFIELDs, que nombran las columnas de esa tabla.
    // Nuestro documento no tiene tales campos, pero sí tiene etiquetas de texto simple encerradas entre llaves.
    // Si establecemos el indicador "PreserveUnusedTags" en "verdadero", podríamos tratar estas etiquetas como MERGEFIELDs
    // para permitir que nuestra combinación de correspondencia inserte datos de la fuente de datos en esas etiquetas.
    // Si establecemos el indicador "PreserveUnusedTags" en "falso",
    // la combinación de correspondencia convertirá estas etiquetas en MERGEFIELDs y las dejará sin completar.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    //Nuestro documento tiene una etiqueta para una columna llamada "Columna2", que no existe en la tabla.
    // Si establecemos el indicador "PreserveUnusedTags" en "falso", then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Cree un documento y agregue dos etiquetas de texto sin formato que puedan actuar como MERGEFIELD durante una combinación de correspondencia.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Nuestras etiquetas se registrarán como destinos para datos de combinación de correspondencia solo si establecemos esto como verdadero.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// Crea una tabla de datos simple con una columna.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### Ver también

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
