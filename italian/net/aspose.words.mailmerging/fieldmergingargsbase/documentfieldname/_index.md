---
title: FieldMergingArgsBase.DocumentFieldName
second_title: Aspose.Words per .NET API Reference
description: FieldMergingArgsBase proprietà. Ottiene il nome del campo di unione come specificato nel documento.
type: docs
weight: 20
url: /it/net/aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/
---
## FieldMergingArgsBase.DocumentFieldName property

Ottiene il nome del campo di unione come specificato nel documento.

```csharp
public string DocumentFieldName { get; }
```

### Osservazioni

Se disponi di una mappatura da un nome di campo di un documento a un nome di campo di origine dati diverso, , questo è il nome di campo originale come specificato nel documento.

Se hai specificato un prefisso per il nome del campo, ad esempio "Immagine:MyFieldName" nel documento, allora`DocumentFieldName` restituisce il nome del campo senza prefisso, ovvero "MyFieldName".

### Esempi

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

* class [FieldMergingArgsBase](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* assemblea [Aspose.Words](../../../)


