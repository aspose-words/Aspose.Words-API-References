---
title: IFieldMergingCallback.ImageFieldMerging
linktitle: ImageFieldMerging
articleTitle: ImageFieldMerging
second_title: Aspose.Words para .NET
description: Descubra el método ImageFieldMerging en IFieldMergingCallback, diseñado para la inserción fluida de imágenes en la combinación de correspondencia de Aspose.Words. ¡Mejore la automatización de sus documentos!
type: docs
weight: 20
url: /es/net/aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/
---
## IFieldMergingCallback.ImageFieldMerging method

Se llama cuando el motor de combinación de correspondencia Aspose.Words está a punto de insertar una imagen en un campo de combinación.

```csharp
public void ImageFieldMerging(ImageFieldMergingArgs args)
```

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

* class [ImageFieldMergingArgs](../../imagefieldmergingargs/)
* interface [IFieldMergingCallback](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
