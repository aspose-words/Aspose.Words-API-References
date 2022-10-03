---
title: IFieldMergingCallback
second_title: Aspose.Words per .NET API Reference
description: Implementa questa interfaccia se desideri controllare come i dati vengono inseriti nei campi di unione durante unoperazione di stampa unione.
type: docs
weight: 3570
url: /it/net/aspose.words.mailmerging/ifieldmergingcallback/
---
## IFieldMergingCallback interface

Implementa questa interfaccia se desideri controllare come i dati vengono inseriti nei campi di unione durante un'operazione di stampa unione.

```csharp
public interface IFieldMergingCallback
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [FieldMerging](../../aspose.words.mailmerging/ifieldmergingcallback/fieldmerging/)(FieldMergingArgs) | Chiamato quando il motore di stampa unione di Aspose.Words sta per inserire dati in un campo di unione nel documento. |
| [ImageFieldMerging](../../aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/)(ImageFieldMergingArgs) | Chiamato quando il motore di stampa unione di Aspose.Words sta per inserire un'immagine in un campo di unione. |

### Esempi

Mostra come inserire in un report le immagini archiviate in un campo BLOB del database.

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

        // Apre il lettore di dati, che deve essere in una modalità che legga tutti i record contemporaneamente.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Fare niente.
    }

    /// <summary>
    /// Viene chiamato quando una stampa unione incontra un MERGEFIELD nel documento con un tag "Image:" nel nome.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

Mostra come eseguire una stampa unione con una richiamata personalizzata che gestisce i dati di unione sotto forma di documenti HTML.

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
/// Se la stampa unione incontra un MERGEFIELD il cui nome inizia con il prefisso "html_",
/// questo callback analizza i dati di unione come contenuto HTML e aggiunge il risultato alla posizione del documento di MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Chiamato quando una stampa unione unisce i dati in un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Aggiunge dati HTML analizzati al corpo del documento.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Poiché abbiamo già inserito manualmente il contenuto unito,
             // non avremo bisogno di rispondere a questo evento restituendo il contenuto tramite la proprietà "Testo".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Fare niente.
    }
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
