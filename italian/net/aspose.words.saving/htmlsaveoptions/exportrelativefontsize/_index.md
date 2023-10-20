---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportRelativeFontSize proprietà. Specifica se le dimensioni dei caratteri devono essere visualizzate in unità relative durante il salvataggio in HTML MHTML o EPUB. Limpostazione predefinita èfalso  in C#.
type: docs
weight: 230
url: /it/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Specifica se le dimensioni dei caratteri devono essere visualizzate in unità relative durante il salvataggio in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## Osservazioni

In molti documenti esistenti (HTML, IDPF EPUB) le dimensioni dei caratteri sono specificate in unità relative. Ciò consente alle applicazioni di regolare la dimensione del testo durante la visualizzazione/elaborazione dei documenti. Ad esempio, Microsoft Internet Explorer ha il sottomenu "Visualizza-&gt;Dimensione testo", Adobe Digital Editions ha due pulsanti: Aumenta/Diminuisci dimensione testo. Se prevedi che questa funzionalità funzioni, imposta`ExportRelativeFontSize` proprietà a`VERO` .

Il modello di documento Aspose Words contiene e funziona solo con unità di dimensione del carattere assoluto. Le unità relative necessitano di logica aggiuntiva per essere ricalcolate da una dimensione iniziale (standard). Dimensione carattere di**Normale** lo stile del documento viene preso come standard. Ad esempio, se**Normale** ha un carattere da 12 punti e parte del testo è da 18 punti, verrà visualizzato come**1,5 em.** all'HTML.

Quando questa opzione è abilitata, gli elementi del documento diversi dal testo avranno comunque dimensioni assolute. Inoltre alcuni attributi relativi al testo potrebbero essere espressi in modo assoluto. In particolare, l'interlinea specificata con la regola "esattamente" potrebbe produrre risultati indesiderati durante il ridimensionamento del testo. Pertanto i documenti di origine dovrebbero essere progettati e testati adeguatamente durante l'esportazione con`ExportRelativeFontSize` impostato`VERO`.

## Esempi

Mostra come utilizzare le dimensioni relative dei caratteri durante il salvataggio in .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare se utilizzare dimensioni dei caratteri relative o assolute.
// Imposta il flag "ExportRelativeFontSize" su "true" per dichiarare le dimensioni dei caratteri
 // utilizzando l'unità di misura "em", che è un fattore che moltiplica la dimensione del carattere corrente.
// Imposta il flag "ExportRelativeFontSize" su "false" per dichiarare le dimensioni dei caratteri
// utilizzando l'unità di misura "pt", che è la dimensione assoluta del carattere in punti.
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
