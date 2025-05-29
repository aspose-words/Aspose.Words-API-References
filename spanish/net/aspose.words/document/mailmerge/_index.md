---
title: Document.MailMerge
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words para .NET
description: Descubra la automatización perfecta de documentos con el objeto MailMerge, mejorando su flujo de trabajo al simplificar las tareas de combinación de correspondencia sin esfuerzo.
type: docs
weight: 270
url: /es/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Devuelve un[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) objeto que representa la funcionalidad de combinación de correspondencia para el documento.

```csharp
public MailMerge MailMerge { get; }
```

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de una DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    A continuación se muestran dos formas de utilizar una DataTable como fuente de datos para una combinación de correspondencia.
    // 1 - Utilice la tabla completa para la combinación de correspondencia para crear un documento de combinación de correspondencia de salida para cada fila de la tabla:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilice una fila de la tabla para crear un documento de combinación de correspondencia de salida:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento fuente de combinación de correspondencia.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Ver también

* class [MailMerge](../../../aspose.words.mailmerging/mailmerge/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
