---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImagesFolderAlias di HtmlSaveOptions per gestire facilmente gli URI delle immagini nei tuoi documenti HTML. Semplifica il tuo flusso di lavoro con questa funzionalità essenziale!
type: docs
weight: 370
url: /it/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI delle immagini scritti in un documento HTML. Il valore predefinito è una stringa vuota.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) in formato HTML, Aspose.Words deve salvare tutte le immagini x000d incorporate nel documento come file autonomi.[`ImagesFolder`](../imagesfolder/) consente di specificare dove verranno salvate le immagini e`ImagesFolderAlias` consente di specificare come verranno costruiti gli URI delle immagini.

Se`ImagesFolderAlias` non è una stringa vuota, allora l'URI dell'immagine scritto in HTML saràImagesFolderAlias + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias`è una stringa vuota, quindi l'URI dell'immagine scritto in HTML saràImagesFolder + &lt;nome file immagine&gt;.

Se`ImagesFolderAlias` è impostato su '.' (punto), il file immagine name verrà scritto in HTML senza percorso, indipendentemente dalle altre opzioni.

Un modo alternativo per specificare il nome della cartella per costruire l'immagine URIs è usare[`ResourceFolderAlias`](../resourcefolderalias/).

## Esempi

Mostra come impostare cartelle e alias di cartelle per le risorse salvate esternamente che Aspose.Words creerà quando si salva un documento in HTML.

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
    FontsFolderAlias = "http://esempio.com/font",
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
