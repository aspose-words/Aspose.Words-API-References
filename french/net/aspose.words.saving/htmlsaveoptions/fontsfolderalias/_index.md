---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words pour .NET
description: Découvrez la propriété HtmlSaveOptions FontsFolderAlias pour personnaliser les URI des polices dans vos documents HTML. Améliorez facilement votre site web !
type: docs
weight: 320
url: /fr/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Spécifie le nom du dossier utilisé pour construire les URI de police écrites dans un document HTML. La valeur par défaut est une chaîne vide.

```csharp
public string FontsFolderAlias { get; set; }
```

## Remarques

Lorsque vous enregistrez un[`Document`](../../../aspose.words/document/) au format HTML et[`ExportFontResources`](../exportfontresources/) est défini sur`vrai` Aspose.Words doit enregistrer les polices utilisées dans le document sous forme de fichiers autonomes. [`FontsFolder`](../fontsfolder/) vous permet de spécifier où les polices seront enregistrées et `FontsFolderAlias` permet de spécifier comment les URI des polices seront construites.

Si`FontsFolderAlias` n'est pas une chaîne vide, alors l'URI de police written en HTML seraFontsFolderAlias + &lt;nom du fichier de police&gt;.

Si`FontsFolderAlias` est une chaîne vide, alors l'URI de police written en HTML seraFontsFolder + &lt;nom du fichier de police&gt;.

Si`FontsFolderAlias`est défini sur '.' (point), alors le nom du fichier de police sera écrit en HTML sans chemin, quelles que soient les autres options.

Une autre façon de spécifier le nom du dossier pour construire les URI de polices est d'utiliser[`ResourceFolderAlias`](../resourcefolderalias/).

## Exemples

Montre comment définir des dossiers et des alias de dossiers pour les ressources enregistrées en externe qu'Aspose.Words créera lors de l'enregistrement d'un document au format HTML.

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
    FontsFolderAlias = "http://exemple.com/fonts",
    ImagesFolderAlias = "http://exemple.com/images",
    ResourceFolderAlias = "http://exemple.com/ressources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Voir également

* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
