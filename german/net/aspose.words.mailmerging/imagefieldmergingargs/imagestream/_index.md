---
title: ImageFieldMergingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words für .NET
description: ImageFieldMergingArgs ImageStream eigendom. Gibt den Stream an aus dem die SerienbriefEngine ein Bild lesen soll in C#.
type: docs
weight: 40
url: /de/net/aspose.words.mailmerging/imagefieldmergingargs/imagestream/
---
## ImageFieldMergingArgs.ImageStream property

Gibt den Stream an, aus dem die Serienbrief-Engine ein Bild lesen soll.

```csharp
public Stream ImageStream { get; set; }
```

## Bemerkungen

Aspose.Words schließt diesen Stream, nachdem das Bild in das Dokument eingefügt wurde.

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

* class [ImageFieldMergingArgs](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
