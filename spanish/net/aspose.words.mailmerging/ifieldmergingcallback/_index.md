---
title: IFieldMergingCallback
second_title: Referencia de API de Aspose.Words para .NET
description: Implemente esta interfaz si desea controlar cómo se insertan los datos en los campos de combinación durante una operación de combinación de correspondencia.
type: docs
weight: 3570
url: /es/net/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface

Implemente esta interfaz si desea controlar cómo se insertan los datos en los campos de combinación durante una operación de combinación de correspondencia.

```csharp
public interface IFieldMergingCallback
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| [FieldMerging](../../aspose.words.mailmerging/ifieldmergingcallback/fieldmerging)(FieldMergingArgs) | Llamado cuando el motor de combinación de correspondencia de Aspose.Words está a punto de insertar datos en un campo de combinación en el documento. |
| [ImageFieldMerging](../../aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging)(ImageFieldMergingArgs) | Llamado cuando el motor de combinación de correspondencia de Aspose.Words está a punto de insertar una imagen en un campo de combinación. |

### Ejemplos

Muestra cómo insertar imágenes almacenadas en un campo BLOB de base de datos en un informe.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Abra el lector de datos, que debe estar en un modo que lea todos los registros a la vez.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Hacer nada.
    }

    /// <summary>
    /// Esto se llama cuando una combinación de correspondencia encuentra un MERGEFIELD en el documento con una etiqueta "Imagen:" en su nombre.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

Muestra cómo ejecutar una combinación de correo con una devolución de llamada personalizada que maneja los datos combinados en forma de documentos HTML.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Si la combinación de correspondencia encuentra un MERGEFIELD cuyo nombre comienza con el prefijo "html_",
/// esta devolución de llamada analiza sus datos combinados como contenido HTML y agrega el resultado a la ubicación del documento de MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Llamado cuando una combinación de correo combina datos en un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Agregar datos HTML analizados al cuerpo del documento.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Dado que ya hemos insertado el contenido fusionado manualmente,
              // no necesitaremos responder a este evento devolviendo contenido a través de la propiedad "Texto".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hacer nada.
    }
}
```

### Ver también

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
