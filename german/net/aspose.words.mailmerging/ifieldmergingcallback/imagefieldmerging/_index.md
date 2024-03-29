---
title: IFieldMergingCallback.ImageFieldMerging
linktitle: ImageFieldMerging
articleTitle: ImageFieldMerging
second_title: Aspose.Words für .NET
description: IFieldMergingCallback ImageFieldMerging methode. Wird aufgerufen wenn die MailMergeEngine von Aspose.Words im Begriff ist ein Bild in ein Serienbrieffeld einzufügen in C#.
type: docs
weight: 20
url: /de/net/aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/
---
## IFieldMergingCallback.ImageFieldMerging method

Wird aufgerufen, wenn die Mail-Merge-Engine von Aspose.Words im Begriff ist, ein Bild in ein Serienbrieffeld einzufügen.

```csharp
public void ImageFieldMerging(ImageFieldMergingArgs args)
```

## Beispiele

Zeigt, wie in einem Datenbank-BLOB-Feld gespeicherte Bilder in einen Bericht eingefügt werden.

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

        // Öffnen Sie den Datenleser, der sich in einem Modus befinden muss, der alle Datensätze auf einmal liest.
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
        // Nichts tun.
    }

    /// <summary>
    /// Dies wird aufgerufen, wenn ein Serienbrief im Dokument auf ein MERGEFIELD mit einem „Image:“-Tag im Namen trifft.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Siehe auch

* class [ImageFieldMergingArgs](../../imagefieldmergingargs/)
* interface [IFieldMergingCallback](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
