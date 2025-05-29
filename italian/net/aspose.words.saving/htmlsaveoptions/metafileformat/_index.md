---
title: HtmlSaveOptions.MetafileFormat
linktitle: MetafileFormat
articleTitle: MetafileFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà HtmlSaveOptions MetafileFormat per esportare in HTML, MHTML o EPUB. Salva i metafile come immagini PNG di alta qualità per impostazione predefinita!
type: docs
weight: 380
url: /it/net/aspose.words.saving/htmlsaveoptions/metafileformat/
---
## HtmlSaveOptions.MetafileFormat property

Specifica in quale formato vengono salvati i metafile durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito èPng , il che significa che i metafile vengono renderizzati in immagini PNG raster.

```csharp
public HtmlMetafileFormat MetafileFormat { get; set; }
```

## Osservazioni

I metafile non vengono visualizzati in modo nativo dai browser HTML. Per impostazione predefinita, Aspose.Words converte le immagini WMF ed EMF in file PNG durante l'esportazione in HTML. Altre opzioni sono la conversione dei metafile in immagini SVG o l'esportazione senza conversione.

Alcune trasformazioni delle immagini, in particolare il ritaglio delle immagini, non verranno applicate alle immagini metafile se vengono esportate in HTML senza conversione.

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

* property [ImageResolution](../imageresolution/)
* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
