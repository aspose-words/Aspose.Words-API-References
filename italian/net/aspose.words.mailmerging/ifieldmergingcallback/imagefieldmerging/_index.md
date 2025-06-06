---
title: IFieldMergingCallback.ImageFieldMerging
linktitle: ImageFieldMerging
articleTitle: ImageFieldMerging
second_title: Aspose.Words per .NET
description: Scopri il metodo ImageFieldMerging in IFieldMergingCallback, progettato per un inserimento di immagini fluido nella stampa unione di Aspose.Words. Migliora l'automazione dei tuoi documenti!
type: docs
weight: 20
url: /it/net/aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/
---
## IFieldMergingCallback.ImageFieldMerging method

Chiamato quando il motore di stampa unione Aspose.Words sta per inserire un'immagine in un campo di unione.

```csharp
public void ImageFieldMerging(ImageFieldMergingArgs args)
```

## Esempi

Mostra come inserire in un report le immagini memorizzate in un campo BLOB del database.

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

        // Aprire il lettore dati, che deve essere in una modalità che legge tutti i record contemporaneamente.
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
        // Non fare nulla.
    }

    /// <summary>
    /// Questa funzione viene chiamata quando una stampa unione incontra un MERGEFIELD nel documento con un tag "Image:" nel nome.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Guarda anche

* class [ImageFieldMergingArgs](../../imagefieldmergingargs/)
* interface [IFieldMergingCallback](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
