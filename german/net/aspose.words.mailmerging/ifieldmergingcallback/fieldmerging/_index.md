---
title: IFieldMergingCallback.FieldMerging
linktitle: FieldMerging
articleTitle: FieldMerging
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumenten-Workflows mit der iFieldMergingCallback-Methode. Integrieren Sie Daten nahtlos in Ihre Aspose.Words-Serienbrieffelder für mehr Effizienz.
type: docs
weight: 10
url: /de/net/aspose.words.mailmerging/ifieldmergingcallback/fieldmerging/
---
## IFieldMergingCallback.FieldMerging method

Wird aufgerufen, wenn die Seriendruck-Engine von Aspose.Words dabei ist, Daten in ein Seriendruckfeld im Dokument einzufügen.

```csharp
public void FieldMerging(FieldMergingArgs args)
```

## Beispiele

Zeigt, wie in einem BLOB-Feld einer Datenbank gespeicherte Bilder in einen Bericht eingefügt werden.

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

        // Öffnen Sie den Datenleser, der sich in einem Modus befinden muss, der alle Datensätze gleichzeitig liest.
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
    /// Dies wird aufgerufen, wenn ein Serienbrief auf ein MERGEFIELD im Dokument trifft, dessen Name ein „Image:“-Tag enthält.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

Zeigt, wie ein Serienbrief mit einem benutzerdefinierten Rückruf ausgeführt wird, der Serienbriefdaten in Form von HTML-Dokumenten verarbeitet.

```csharp
public void MergeHtml()
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
/// Wenn der Serienbrief auf ein MERGEFIELD trifft, dessen Name mit dem Präfix "html_" beginnt,
/// Dieser Rückruf analysiert seine Zusammenführungsdaten als HTML-Inhalt und fügt das Ergebnis zum Dokumentspeicherort des MERGEFIELD hinzu.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in ein MERGEFIELD zusammenführt.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Fügen Sie dem Hauptteil des Dokuments analysierte HTML-Daten hinzu.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Da wir den zusammengeführten Inhalt bereits manuell eingefügt haben,
            // Wir müssen auf dieses Ereignis nicht reagieren, indem wir Inhalte über die Eigenschaft „Text“ zurückgeben.
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Nichts tun.
    }
}
```

### Siehe auch

* class [FieldMergingArgs](../../fieldmergingargs/)
* interface [IFieldMergingCallback](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
