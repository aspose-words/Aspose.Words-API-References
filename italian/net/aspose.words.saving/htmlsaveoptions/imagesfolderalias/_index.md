---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ImagesFolderAlias proprietà. Specifica il nome della cartella utilizzata per costruire gli URI di immagine scritti in un documento HTML. Il valore predefinito è una stringa vuota in C#.
type: docs
weight: 370
url: /it/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI di immagine scritti in un documento HTML. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un file[`Document`](../../../aspose.words/document/) in formato HTML, Aspose.Words deve salvare tutte le immagini incorporate nel documento come file autonomi.[`ImagesFolder`](../imagesfolder/) ti consente di specificare dove verranno salvate le immagini e`ImagesFolderAlias` consente di specificare come verranno costruiti gli URI dell'immagine.

Se`ImagesFolderAlias` non è una stringa vuota, lo sarà l'URI dell'immagine scritto in HTMLImagesFolderAlias + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias` è una stringa vuota, l'URI dell'immagine scritto in HTML saràCartella Immagini + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias`è impostato per '.' (punto), il nome del file immagine verrà scritto in HTML senza percorso indipendentemente dalle altre opzioni.

Un modo alternativo per specificare il nome della cartella per costruire gli URI dell'immagine è utilizzare[`ResourceFolderAlias`](../resourcefolderalias/).

## Esempi

Mostra come impostare cartelle e alias di cartelle per le risorse salvate esternamente che Aspose.Words creerà durante il salvataggio di un documento in HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://esempio.com/fonts",
    ImagesFolderAlias = "http://esempio.com/immagini",
    ResourceFolderAlias = "http://esempio.com/risorse",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
