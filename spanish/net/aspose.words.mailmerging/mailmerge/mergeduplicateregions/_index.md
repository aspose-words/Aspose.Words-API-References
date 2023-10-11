---
title: MailMerge.MergeDuplicateRegions
second_title: Referencia de API de Aspose.Words para .NET
description: MailMerge propiedad. Obtiene o establece un valor que indica si todas las regiones de combinación de correspondencia del documento con el nombre de una fuente de datos deben fusionarse al ejecutar una combinación de correspondencia con regiones en la fuente de datos o solo la primera.
type: docs
weight: 60
url: /es/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Obtiene o establece un valor que indica si todas las regiones de combinación de correspondencia del documento con el nombre de una fuente de datos deben fusionarse al ejecutar una combinación de correspondencia con regiones en la fuente de datos o solo la primera.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

### Observaciones

El valor predeterminado es`FALSO` .

### Ejemplos

Muestra cómo trabajar con regiones de combinación de correspondencia duplicadas.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // Si configuramos la propiedad "MergeDuplicateRegions" en "falso", la combinación de correspondencia afectará a la primera región,
    // mientras que los MERGEFIELD del segundo se dejarán en el estado previo a la fusión.
    // Para fusionar ambas regiones de esa manera,
    // tendríamos que ejecutar la combinación de correspondencia dos veces en una tabla del mismo nombre.
    // Si configuramos la propiedad "MergeDuplicateRegions" en "true", la combinación de correspondencia afectará a ambas regiones.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Devuelve un documento que contiene dos regiones de combinación de correspondencia duplicadas (que comparten el mismo nombre en las etiquetas "TableStart/End").
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// Crea una tabla de datos con una fila y dos columnas.
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)


