---
title: Enum HtmlMetafileFormat
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.HtmlMetafileFormat enum. Indica il formato in cui i metafile vengono salvati nei documenti HTML.
type: docs
weight: 5090
url: /it/net/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enumeration

Indica il formato in cui i metafile vengono salvati nei documenti HTML.

```csharp
public enum HtmlMetafileFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Png | `0` | I metafile vengono renderizzati in immagini PNG raster. |
| Svg | `1` | I metafile vengono convertiti in immagini SVG vettoriali. |
| EmfOrWmf | `2` | I metafile vengono salvati così come sono, senza conversione. |

### Esempi

Mostra come convertire gli oggetti SVG in un formato diverso durante il salvataggio di documenti HTML.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' larghezza='500' altezza='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Utilizza 'ConvertSvgToEmf' per ripristinare il comportamento legacy
// dove tutte le immagini SVG caricate da un documento HTML sono state convertite in EMF.
// Ora le immagini SVG vengono caricate senza conversione
// se la versione di MS Word specificata nelle opzioni di caricamento supporta le immagini SVG in modo nativo.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Questo documento contiene un file <svg> elemento sotto forma di testo.
// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare come l'operazione di salvataggio gestisce questo oggetto.
// Impostazione della proprietà "MetafileFormat" su "HtmlMetafileFormat.Png" per convertirla in un'immagine PNG.
// Impostando la proprietà "MetafileFormat" su "HtmlMetafileFormat.Svg" preservala come oggetto SVG.
// Impostazione della proprietà "MetafileFormat" su "HtmlMetafileFormat.EmfOrWmf" per convertirla in un metafile.
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
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" versione=\"1.1\" larghezza=\"499\" altezza= \"40\">"));
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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


