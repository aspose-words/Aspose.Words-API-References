---
title: FieldMergingArgs Class
linktitle: FieldMergingArgs
articleTitle: FieldMergingArgs
second_title: Aspose.Words per .NET
description: Aspose.Words.MailMerging.FieldMergingArgs classe. Fornisce i dati per ilUnisci campo evento in C#.
type: docs
weight: 3770
url: /it/net/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class

Fornisce i dati per il**Unisci campo** evento.

Per saperne di più, visita il[Stampa unione e reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

```csharp
public class FieldMergingArgs : FieldMergingArgsBase
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Restituisce il[`Document`](../fieldmergingargsbase/document/) oggetto per cui viene eseguita la stampa unione. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Ottiene il nome del campo di unione come specificato nel documento. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Ottiene l'oggetto che rappresenta il campo di unione corrente. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Ottiene il nome del campo di unione nell'origine dati. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Ottiene o imposta il valore del campo dall'origine dati. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Ottiene l'indice in base zero del record da unire. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Ottiene il nome della tabella dati per l'operazione di unione corrente o una stringa vuota se il nome non è disponibile. |
| [Text](../../aspose.words.mailmerging/fieldmergingargs/text/) { get; set; } | Ottiene o imposta il testo che verrà inserito nel documento per il campo di unione corrente. |

## Osservazioni

IL**Unisci campo** L'evento si verifica durante la stampa unione quando nel documento viene rilevato un semplice campo mail merge . Puoi rispondere a questo evento per restituire il testo che il motore di stampa unione dovrà inserire nel documento.

## Esempi

Mostra come eseguire una stampa unione con un callback personalizzato che gestisce i dati di unione sotto forma di documenti HTML.

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
             // non avremo bisogno di rispondere a questo evento restituendo il contenuto tramite la proprietà "Text".
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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)
