---
title: MarkdownSaveOptions Class
linktitle: MarkdownSaveOptions
articleTitle: MarkdownSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.Saving.MarkdownSaveOptions pour un enregistrement optimisé de vos documents au format Markdown. Personnalisez vos résultats avec des options avancées dès aujourd'hui !
type: docs
weight: 6060
url: /fr/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

Classe permettant de spécifier des options supplémentaires lors de l'enregistrement d'un document dans leMarkdown format.

Pour en savoir plus, visitez le[Spécifier les options d'enregistrement](https://docs.aspose.com/words/net/specify-save-options/) article de documentation.

```csharp
public class MarkdownSaveOptions : TxtSaveOptionsBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [MarkdownSaveOptions](markdownsaveoptions/)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leMarkdown format. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est`FAUX` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est**chaîne vide** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les effets 3D sont rendus. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les formes DrawingML sont rendues. |
| [EmptyParagraphExportMode](../../aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/) { get; set; } | Spécifie comment exporter les paragraphes vides vers Markdown. La valeur par défaut estEmptyLine . |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Spécifie l'encodage à utiliser lors de l'exportation au format texte. La valeur par défaut est**Codage.UTF8** . |
| [ExportAsHtml](../../aspose.words.saving/markdownsaveoptions/exportashtml/) { get; set; } | Permet de spécifier les éléments à exporter vers Markdown sous forme de HTML brut. La valeur par défaut estNone . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quand`vrai` , provoque l'intégration du nom et de la version d'Aspose.Words dans les fichiers produits. La valeur par défaut est`vrai` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Spécifie la manière dont les en-têtes et les pieds de page sont exportés vers les formats texte. La valeur par défaut estPrimaryOnly . |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | Spécifie si les images sont enregistrées au format Base64 dans le fichier de sortie. La valeur par défaut est`FAUX` . |
| [ExportUnderlineFormatting](../../aspose.words.saving/markdownsaveoptions/exportunderlineformatting/) { get; set; } | Obtient ou définit une valeur booléenne indiquant d'exporter le formatage du texte souligné sous forme de séquence de deux caractères plus "++". La valeur par défaut est`FAUX` . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Permet de spécifier si les sauts de page doivent être conservés lors de l'export. |
| [ImageResolution](../../aspose.words.saving/markdownsaveoptions/imageresolution/) { get; set; } | Spécifie la résolution de sortie des images lors de l'exportation vers Markdown. La valeur par défaut est`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | Permet de contrôler la manière dont les images sont enregistrées lorsqu'un document est enregistré dans Markdown format. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | Spécifie le dossier physique dans lequel les images sont enregistrées lors de l'exportation d'un document vers leMarkdown format. La valeur par défaut est une chaîne vide. |
| [ImagesFolderAlias](../../aspose.words.saving/markdownsaveoptions/imagesfolderalias/) { get; set; } | Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document. La valeur par défaut est une chaîne vide. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les objets d'encre (InkML) sont rendus. |
| [LinkExportMode](../../aspose.words.saving/markdownsaveoptions/linkexportmode/) { get; set; } | Spécifie comment les liens seront écrits dans le fichier de sortie. La valeur par défaut estAuto . |
| [ListExportMode](../../aspose.words.saving/markdownsaveoptions/listexportmode/) { get; set; } | Spécifie comment les éléments de la liste seront écrits dans le fichier de sortie. La valeur par défaut estMarkdownSyntax . |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit une valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est`FAUX` . |
| [OfficeMathExportMode](../../aspose.words.saving/markdownsaveoptions/officemathexportmode/) { get; set; } | Spécifie comment OfficeMath sera écrit dans le fichier de sortie. La valeur par défaut estText . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Spécifie la chaîne à utiliser comme saut de paragraphe lors de l'exportation au format texte. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , joli format de sortie le cas échéant. La valeur par défaut est`FAUX` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreMarkdown . |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | Obtient ou définit une valeur qui spécifie comment aligner le contenu des tables lors de l'exportation vers leMarkdown format. La valeur par défaut estAuto . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est`FAUX` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est`vrai` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

## Exemples

Montre comment renommer le nom de l'image lors de l'enregistrement dans un document Markdown.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Si nous convertissons un document contenant des images en Markdown, nous nous retrouverons avec un fichier Markdown contenant des liens vers plusieurs images.
    // Chaque image sera sous la forme d'un fichier dans le système de fichiers local.
    // Il existe également un rappel qui peut personnaliser le nom et l'emplacement du système de fichiers de chaque image.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // La méthode ImageSaving() de notre rappel sera exécutée à ce moment.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// Renomme les images enregistrées qui sont produites lors de l'enregistrement d'un document Markdown.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        args.ImageFileName = imageFileName;
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Voir également

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
