---
title: ImageFieldMergingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ImageStream de ImageFieldMergingArgs mejora su combinación de correspondencia al integrar imágenes sin problemas para obtener resultados profesionales.
type: docs
weight: 40
url: /es/net/aspose.words.mailmerging/imagefieldmergingargs/imagestream/
---
## ImageFieldMergingArgs.ImageStream property

Especifica la secuencia desde la cual el motor de combinación de correspondencia leerá una imagen.

```csharp
public Stream ImageStream { get; set; }
```

## Observaciones

Aspose.Words cierra esta secuencia después de fusionar la imagen en el documento.

## Ejemplos

Muestra cómo insertar imágenes almacenadas en un campo BLOB de base de datos en un informe.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
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
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        //No hacer nada.
    }

    /// <summary>
    /// Esto se llama cuando una combinación de correspondencia encuentra un MERGEFIELD en el documento con una etiqueta "Image:" en su nombre.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Ver también

* class [ImageFieldMergingArgs](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
