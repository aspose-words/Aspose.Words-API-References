---
title: FieldMergingArgs.Text
second_title: Aspose.Words per .NET API Reference
description: FieldMergingArgs proprietà. Ottiene o imposta il testo che verrà inserito nel documento per il campo di unione corrente.
type: docs
weight: 10
url: /it/net/aspose.words.mailmerging/fieldmergingargs/text/
---
## FieldMergingArgs.Text property

Ottiene o imposta il testo che verrà inserito nel documento per il campo di unione corrente.

```csharp
public string Text { get; set; }
```

### Osservazioni

Quando viene chiamato il gestore dell'evento, questa proprietà è impostata su null.

Se lasci il testo come null, il motore di stampa unione verrà inserito[`FieldValue`](../../fieldmergingargsbase/fieldvalue/) al posto del campo di unione.

Se imposti Testo su qualsiasi stringa (anche vuota), la stringa verrà inserita nel documento al posto del campo di unione.

### Esempi

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

* class [FieldMergingArgs](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../fieldmergingargs/)
* assemblea [Aspose.Words](../../../)


