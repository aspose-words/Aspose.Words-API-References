---
title: HtmlSaveOptions.ExportRoundtripInformation
linktitle: ExportRoundtripInformation
articleTitle: ExportRoundtripInformation
second_title: Aspose.Words per .NET
description: Scopri la proprietà ExportRoundtripInformation di HtmlSaveOptions per controllare i dati di andata e ritorno nei formati HTML, MHTML ed EPUB. Ottimizza le tue esportazioni oggi stesso!
type: docs
weight: 240
url: /it/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Specifica se scrivere le informazioni di andata e ritorno durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è`VERO` per HTML e`falso` per MHTML ed EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

## Osservazioni

Il salvataggio delle informazioni di andata e ritorno consente di ripristinare le proprietà del documento come tabulazioni, commenti, intestazioni e piè di pagina durante il caricamento dei documenti HTML in un[`Document`](../../../aspose.words/document/) oggetto.

Quando`VERO`, le informazioni sul viaggio di andata e ritorno vengono esportate come -aw-* CSS properties degli elementi HTML corrispondenti.

Quando`falso`, fa sì che nessuna informazione sul viaggio di andata e ritorno venga emessa nei file prodotti.

## Esempi

Mostra come preservare gli elementi nascosti durante la conversione in .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Quando si converte un documento in .html, alcuni elementi come i segnalibri nascosti, le posizioni delle forme originali,
// oppure le note a piè di pagina verranno rimosse o convertite in testo normale e di fatto andranno perse.
// Il salvataggio con un oggetto HtmlSaveOptions con ExportRoundtripInformation impostato su true conserverà questi elementi.

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per determinare
// come l'operazione di salvataggio esporterà gli elementi del documento che HTML non supporta o non utilizza,
// come segnalibri nascosti e posizioni delle forme originali.
// Se impostiamo il flag "ExportRoundtripInformation" su "true", l'operazione di salvataggio conserverà questi elementi.
// Se impostiamo il flag "ExportRoundTripInformation" su "false", l'operazione di salvataggio eliminerà questi elementi.
// Vorremo preservare tali elementi se intendiamo caricare l'HTML salvato utilizzando Aspose.Words,
// poiché potrebbero tornare utili ancora una volta.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
