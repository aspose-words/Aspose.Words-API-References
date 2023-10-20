---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportTocPageNumbers proprietà. Specifica se scrivere i numeri di pagina nel sommario durante il salvataggio di HTML MHTML ed EPUB. Il valore predefinito èfalso  in C#.
type: docs
weight: 270
url: /it/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

Specifica se scrivere i numeri di pagina nel sommario durante il salvataggio di HTML, MHTML ed EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## Esempi

Mostra come visualizzare i numeri di pagina quando si salva un documento con un sommario in .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un sommario, quindi popola il documento con paragrafi formattati utilizzando una "Intestazione"
// stile che il sommario prenderà come voci. Ogni voce visualizzerà il paragrafo dell'intestazione a sinistra,
// e il numero di pagina che contiene l'intestazione a destra.
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
// i numeri di pagina visualizzati dal nostro sommario non avranno significato.
// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per omettere questi numeri di pagina dal sommario.
// Se impostiamo il flag "ExportTocPageNumbers" su "true",
// ogni voce del sommario visualizzerà l'intestazione, il separatore e il numero di pagina, preservandone l'aspetto in Microsoft Word.
// Se impostiamo il flag "ExportTocPageNumbers" su "false",
// l'operazione di salvataggio ometterà sia il separatore che il numero di pagina e lascerà intatta l'intestazione di ciascuna voce.
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
