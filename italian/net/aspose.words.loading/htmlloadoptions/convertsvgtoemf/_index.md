---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words per .NET
description: Scopri la proprietà ConvertSvgToEmf di HtmlLoadOptions. Controlla facilmente la conversione da SVG a EMF per una qualità dell'immagine ottimale. Il valore predefinito è "false"; mantieni intatti gli SVG!
type: docs
weight: 30
url: /it/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Ottiene o imposta un valore che indica se convertire le immagini SVG caricate nel formato EMF. Il valore predefinito è`falso` e, se possibile, le immagini SVG caricate vengono memorizzate così come sono, senza conversione.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Osservazioni

Le versioni più recenti di MS Word supportano nativamente le immagini SVG. Se la versione di MS Word specificata nelle opzioni di caricamento supporta SVG, Aspose.Words memorizzerà le immagini SVG così come sono, senza conversione. Se SVG non è supportato, le immagini SVG caricate verranno convertite nel formato EMF.

Se, tuttavia, questa opzione è impostata su`VERO` , Aspose.Words convertirà le immagini SVG caricate in EMF anche se le immagini SVG sono supportate dalla versione specificata di MS Word.

## Esempi

Mostra come convertire gli oggetti SVG in un formato diverso quando si salvano documenti HTML.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Utilizzare 'ConvertSvgToEmf' per ripristinare il comportamento legacy
// dove tutte le immagini SVG caricate da un documento HTML sono state convertite in EMF.
// Ora le immagini SVG vengono caricate senza conversione
// se la versione di MS Word specificata nelle opzioni di caricamento supporta nativamente le immagini SVG.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Questo documento contiene un elemento <svg> sotto forma di testo.
// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare come l'operazione di salvataggio gestisce questo oggetto.
// Impostando la proprietà "MetafileFormat" su "HtmlMetafileFormat.Png" per convertirla in un'immagine PNG.
// Impostando la proprietà "MetafileFormat" su "HtmlMetafileFormat.Svg" la si conserva come oggetto SVG.
// Impostando la proprietà "MetafileFormat" su "HtmlMetafileFormat.EmfOrWmf" per convertirla in un metafile.
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" versione=\"1.1\" larghezza=\"499\" altezza=\"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### Guarda anche

* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
