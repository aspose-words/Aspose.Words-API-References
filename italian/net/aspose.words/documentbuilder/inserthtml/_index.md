---
title: DocumentBuilder.InsertHtml
linktitle: InsertHtml
articleTitle: InsertHtml
second_title: Aspose.Words per .NET
description: Migliora senza sforzo i tuoi documenti con il metodo InsertHtml di DocumentBuilder inserisci senza problemi stringhe HTML per l'integrazione di contenuti dinamici.
type: docs
weight: 380
url: /it/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(*string*) {#inserthtml}

Inserisce una stringa HTML nel documento.

```csharp
public void InsertHtml(string html)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| html | String | Una stringa HTML da inserire nel documento. |

## Osservazioni

Puoi usare questo metodo per inserire un frammento HTML o un intero documento HTML.

## Esempi

Mostra come utilizzare un generatore di documenti per inserire contenuto HTML in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// L'inserimento del codice HTML analizza la formattazione di ciascun elemento nella formattazione del testo del documento equivalente.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

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
/// questa callback analizza i dati di unione come contenuto HTML e aggiunge il risultato alla posizione del documento del MERGEFIELD.
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
            // Aggiungere dati HTML analizzati al corpo del documento.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Poiché abbiamo già inserito manualmente il contenuto unito,
            // non sarà necessario rispondere a questo evento restituendo contenuto tramite la proprietà "Text".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Non fare nulla.
    }
}
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertHtml(*string, bool*) {#inserthtml_2}

Inserisce una stringa HTML nel documento.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| html | String | Una stringa HTML da inserire nel documento. |
| useBuilderFormatting | Boolean | Un valore che indica se la formattazione è specificata in[`DocumentBuilder`](../) viene utilizzato come formattazione di base per il testo importato da HTML. |

## Osservazioni

Puoi usare questo metodo per inserire un frammento HTML o un intero documento HTML.

Quando*useBuilderFormatting* È`falso` , [`DocumentBuilder`](../) La formattazione viene ignorata e la formattazione del testo inserito si basa sulla formattazione HTML predefinita. Di conseguenza, il testo appare come visualizzato nei browser.

Quando*useBuilderFormatting* È`VERO` , la formattazione del testo inserito si basa su[`DocumentBuilder`](../) formattazione, e il testo sembra come se fosse stato inserito con[`Write`](../write/) .

## Esempi

Mostra come applicare la formattazione di un generatore di documenti durante l'inserimento di contenuto HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta un allineamento del testo per il builder, inserisci un paragrafo HTML con un allineamento specificato e uno senza.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Il primo paragrafo ha un allineamento specificato. Quando InsertHtml analizza il codice HTML,
// il valore di allineamento del paragrafo trovato nel codice HTML sostituisce sempre il valore del generatore di documenti.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// Il secondo paragrafo non ha alcun allineamento specificato. È possibile specificare il valore di allineamento.
// in base al valore del builder in base al flag passato al metodo InsertHtml.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertHtml(*string, [HtmlInsertOptions](../../htmlinsertoptions/)*) {#inserthtml_1}

Inserisce una stringa HTML nel documento. Permette di specificare opzioni aggiuntive.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| html | String | Una stringa HTML da inserire nel documento. |
| options | HtmlInsertOptions | Opzioni utilizzate quando viene inserita una stringa HTML. |

## Osservazioni

Puoi usare questo metodo per inserire un frammento HTML o un intero documento HTML.

## Esempi

Mostra come utilizzare le opzioni durante l'inserimento di codice HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// Per impostazione predefinita "DocumentBuilder.InsertHtml" inserisce un frammento HTML che termina con un elemento HTML a livello di blocco,
// normalmente chiude l'elemento a livello di blocco e inserisce un'interruzione di paragrafo.
// Di conseguenza, dopo l'inserimento del documento viene visualizzato un nuovo paragrafo vuoto.
// Se specifichiamo "HtmlInsertOptions.RemoveLastEmptyParagraph", i paragrafi vuoti in eccesso verranno rimossi.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### Guarda anche

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
