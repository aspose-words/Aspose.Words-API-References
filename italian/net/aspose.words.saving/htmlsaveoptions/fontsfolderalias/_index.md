---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words per .NET
description: Scopri la proprietà FontsFolderAlias di HtmlSaveOptions per personalizzare gli URI dei font nei tuoi documenti HTML. Migliora il tuo web design con facilità!
type: docs
weight: 320
url: /it/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI dei font scritti in un documento HTML. Il valore predefinito è una stringa vuota.

```csharp
public string FontsFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un[`Document`](../../../aspose.words/document/) in formato HTML e[`ExportFontResources`](../exportfontresources/) è impostato su`VERO` , Aspose.Words deve salvare i font utilizzati nel documento come file autonomi. [`FontsFolder`](../fontsfolder/) consente di specificare dove verranno salvati i font e `FontsFolderAlias` consente di specificare come verranno costruiti gli URI dei font.

Se`FontsFolderAlias` non è una stringa vuota, allora l'URI del font scritto in HTML saràFontsFolderAlias + &lt;nome file font&gt;.

Se`FontsFolderAlias` è una stringa vuota, quindi l'URI del font scritto in HTML saràFontsFolder + &lt;nome file font&gt;.

Se`FontsFolderAlias`è impostato su '.' (punto), il nome del file del font verrà scritto in HTML senza percorso, indipendentemente dalle altre opzioni.

Un modo alternativo per specificare il nome della cartella per costruire i font URIs è usare[`ResourceFolderAlias`](../resourcefolderalias/).

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
