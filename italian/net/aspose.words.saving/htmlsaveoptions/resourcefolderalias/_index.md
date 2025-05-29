---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words per .NET
description: Ottimizza i tuoi documenti HTML con la proprietà HtmlSaveOptions ResourceFolderAlias, definendo i nomi delle cartelle per una costruzione efficiente degli URI delle risorse.
type: docs
weight: 450
url: /it/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Specifica il nome della cartella utilizzata per costruire gli URI di tutte le risorse scritte in un documento HTML. Il valore predefinito è una stringa vuota.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Osservazioni

`ResourceFolderAlias` è il modo più semplice per specificare come devono essere costruiti gli URI per tutti i file di risorse. Le stesse informazioni possono essere specificate separatamente per immagini e font tramite[`ImagesFolderAlias`](../imagesfolderalias/) e[`FontsFolderAlias`](../fontsfolderalias/) proprietà, rispettivamente. Tuttavia, non esiste una proprietà individuale per CSS.

`ResourceFolderAlias` ha una priorità inferiore a[`FontsFolderAlias`](../fontsfolderalias/) e[`ImagesFolderAlias`](../imagesfolderalias/) Ad esempio, se entrambi`ResourceFolderAlias` e[`FontsFolderAlias`](../fontsfolderalias/) sono specificati, gli URI dei font saranno costruiti usando [`FontsFolderAlias`](../fontsfolderalias/) mentre gli URI delle immagini e dei CSS saranno costruiti utilizzando `ResourceFolderAlias`.

Se`ResourceFolderAlias` è vuoto, il[`ResourceFolder`](../resourcefolder/) il valore della proprietà verrà utilizzato per costruire gli URI delle risorse.

Se`ResourceFolderAlias` è impostato su '.' (punto), gli URI delle risorse conterranno solo nomi di file, senza alcun percorso.

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
