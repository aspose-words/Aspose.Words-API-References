---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad MailMerge MergeWholeDocument actualiza todos los campos durante una combinación de correspondencia basada en regiones, mejorando la eficiencia y la precisión de sus documentos.
type: docs
weight: 70
url: /es/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Obtiene o establece un valor que indica si los campos de todo el documento se actualizan mientras se ejecuta una combinación de correspondencia con regiones.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` .

## Ejemplos

Muestra la relación entre las fusiones de correspondencia con regiones y la actualización de campos.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Si establecemos el indicador "MergeWholeDocument" en "verdadero",
    // La combinación de correspondencia con regiones actualizará todos los campos del documento.
    // Si establecemos el indicador "MergeWholeDocument" en "falso", la combinación de correspondencia solo actualizará los campos
    // dentro de la región de combinación de correspondencia cuyo nombre coincide con el nombre de la tabla de origen de datos.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // La combinación de correspondencia solo actualizará el campo QUOTE fuera de la región de combinación de correspondencia
    // si establecemos el indicador "MergeWholeDocument" en "verdadero".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Cree un documento con una región de combinación de correspondencia que pertenezca a una fuente de datos denominada "MiTabla".
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
/// Cree una tabla de datos que se utilizará en una combinación de correspondencia.
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
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
