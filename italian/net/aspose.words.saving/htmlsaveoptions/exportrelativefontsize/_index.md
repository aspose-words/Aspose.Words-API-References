---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words per .NET
description: Scopri la proprietà ExportRelativeFontSize di HtmlSaveOptions per personalizzare le dimensioni dei caratteri nei formati HTML, MHTML o EPUB. Migliora la leggibilità con facilità!
type: docs
weight: 230
url: /it/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Specifica se le dimensioni del carattere devono essere emesse in unità relative quando si salva in HTML, MHTML o EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## Osservazioni

In molti documenti esistenti (HTML, IDPF EPUB) le dimensioni dei caratteri sono specificate in unità relative. Questo consente alle applicazioni di regolare le dimensioni del testo durante la visualizzazione/elaborazione dei documenti. Ad esempio, Microsoft Internet Explorer ha il sottomenu "Visualizza -&gt; Dimensione testo", mentre Adobe Digital Editions ha due pulsanti: Aumenta/Diminuisci dimensione testo. Se si prevede che questa funzionalità funzioni, impostare`ExportRelativeFontSize` proprietà a`VERO` .

Il modello di documento Aspose Words contiene e funziona solo con unità di dimensione del carattere assolute. Le unità relative necessitano di logica aggiuntiva per essere ricalcolate a partire da una dimensione iniziale (standard). Dimensione del carattere di**Normale** Lo stile del documento è considerato standard. Ad esempio, se**Normale** ha un font da 12 pt e parte del testo è da 18 pt, quindi verrà visualizzato come output **1,5em.** all'HTML.

Quando questa opzione è abilitata, gli elementi del documento diversi dal testo continueranno ad avere dimensioni assolute. Anche alcuni attributi relativi al testo potrebbero essere espressi in modo assoluto. In particolare, l'interlinea specificata con la regola "esatta" potrebbe produrre risultati indesiderati durante il ridimensionamento del testo. Pertanto, i documenti di origine devono essere progettati e testati correttamente durante l'esportazione con`ExportRelativeFontSize` impostato su`VERO`.

## Esempi

Mostra come utilizzare le dimensioni relative dei caratteri quando si salva in formato .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare se utilizzare dimensioni di carattere relative o assolute.
// Imposta il flag "ExportRelativeFontSize" su "true" per dichiarare le dimensioni dei caratteri
 // utilizzando l'unità di misura "em", che è un fattore che moltiplica la dimensione corrente del carattere.
// Imposta il flag "ExportRelativeFontSize" su "false" per dichiarare le dimensioni dei caratteri
// utilizzando l'unità di misura "pt", che è la dimensione assoluta del font in punti.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
