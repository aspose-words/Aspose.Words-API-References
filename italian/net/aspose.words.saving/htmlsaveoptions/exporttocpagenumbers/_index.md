---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: Aspose.Words per .NET
description: Controlla i numeri di pagina del sommario nelle esportazioni HTML, MHTML ed EPUB con HtmlSaveOptions. Migliora la navigazione e l'esperienza utente senza sforzo!
type: docs
weight: 270
url: /it/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

Specifica se scrivere i numeri di pagina nel sommario quando si salva HTML, MHTML ed EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## Esempi

Mostra come visualizzare i numeri di pagina quando si salva un documento con un indice in formato .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un indice e poi popola il documento con paragrafi formattati utilizzando un "Titolo"
// stile che il sommario assumerà come voci. Ogni voce visualizzerà il paragrafo di intestazione a sinistra,
// e il numero di pagina che contiene il titolo sulla destra.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// I documenti HTML non hanno pagine. Se salviamo questo documento in HTML,
// i numeri di pagina visualizzati nel nostro indice non avranno alcun significato.
// Quando salviamo il documento in formato HTML, possiamo passare un oggetto SaveOptions per omettere questi numeri di pagina dall'indice.
// Se impostiamo il flag "ExportTocPageNumbers" su "true",
// ogni voce dell'indice visualizzerà l'intestazione, il separatore e il numero di pagina, mantenendone l'aspetto in Microsoft Word.
// Se impostiamo il flag "ExportTocPageNumbers" su "false",
// l'operazione di salvataggio ometterà sia il separatore sia il numero di pagina e lascerà intatta l'intestazione di ogni voce.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 2</span>" +
        "</p>"));
}
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
