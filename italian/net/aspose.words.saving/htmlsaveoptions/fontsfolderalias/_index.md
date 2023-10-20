---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words per .NET
description: HtmlSaveOptions FontsFolderAlias proprietà. Specifica il nome della cartella utilizzata per costruire gli URI dei caratteri scritti in un documento HTML. Il valore predefinito è una stringa vuota in C#.
type: docs
weight: 320
url: /it/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI dei caratteri scritti in un documento HTML. Il valore predefinito è una stringa vuota.

```csharp
public string FontsFolderAlias { get; set; }
```

## Osservazioni

Quando salvi un file[`Document`](../../../aspose.words/document/) in formato HTML e[`ExportFontResources`](../exportfontresources/) è impostato su`VERO` , Aspose.Words deve salvare i caratteri utilizzati nel documento come file autonomi. [`FontsFolder`](../fontsfolder/) ti permette di specificare dove verranno salvati i caratteri e `FontsFolderAlias` permette di specificare come verranno costruiti gli URI dei caratteri.

Se`FontsFolderAlias` non è una stringa vuota, lo sarà l'URI del carattere scritto in HTMLFontsFolderAlias + &lt;nome file carattere&gt;.

Se`FontsFolderAlias` è una stringa vuota, lo sarà l'URI del carattere scritto in HTMLCartella Fonts + &lt;nome file font&gt;.

Se`FontsFolderAlias`è impostato per '.' (punto), il nome del file del carattere verrà scritto in HTML senza percorso indipendentemente dalle altre opzioni.

Un modo alternativo per specificare il nome della cartella per costruire gli URI del carattere consiste nell'utilizzare[`ResourceFolderAlias`](../resourcefolderalias/).

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
