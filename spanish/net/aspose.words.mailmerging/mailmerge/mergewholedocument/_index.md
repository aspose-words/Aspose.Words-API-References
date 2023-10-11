---
title: MailMerge.MergeWholeDocument
second_title: Referencia de API de Aspose.Words para .NET
description: MailMerge propiedad. Obtiene o establece un valor que indica si los campos de todo el documento se actualizan durante la ejecución de una combinación de correspondencia con regiones.
type: docs
weight: 70
url: /es/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Obtiene o establece un valor que indica si los campos de todo el documento se actualizan durante la ejecución de una combinación de correspondencia con regiones.

```csharp
public bool MergeWholeDocument { get; set; }
```

### Observaciones

El valor predeterminado es`FALSO` .

### Ejemplos

Muestra la relación entre la combinación de correspondencia con las regiones y la actualización de campos.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Si configuramos el indicador "MergeWholeDocument" en "verdadero",
    // la combinación de correspondencia con regiones actualizará todos los campos del documento.
    // Si configuramos el indicador "MergeWholeDocument" en "falso", la combinación de correspondencia solo actualizará los campos
    // dentro de la región de combinación de correspondencia cuyo nombre coincide con el nombre de la tabla de origen de datos.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // La combinación de correspondencia solo actualizará el campo QUOTE fuera de la región de combinación de correspondencia
    // si configuramos el indicador "MergeWholeDocument" en "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Crea un documento con una región de combinación de correspondencia que pertenece a una fuente de datos denominada "MyTable".
/// Inserta un campo QUOTE dentro de esta región y uno más fuera de ella.
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// Crea una tabla de datos que se utilizará en una combinación de correspondencia.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)


