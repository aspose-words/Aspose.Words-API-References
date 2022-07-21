---
title: XamlFlowSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Peut être utilisé pour spécifier des options supplémentaires lors de lenregistrement dun document dans le XamlFlow ouXamlFlowPack format.
type: docs
weight: 5420
url: /fr/net/aspose.words.saving/xamlflowsaveoptions/
---
## XamlFlowSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans le XamlFlow ouXamlFlowPack format.

```csharp
public class XamlFlowSaveOptions : SaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [XamlFlowSaveOptions](xamlflowsaveoptions#constructor)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leXamlFlow format. |
| [XamlFlowSaveOptions](xamlflowsaveoptions#constructor_1)(SaveFormat) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leXamlFlow ouXamlFlowPack format. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **faux** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des formes DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Lorsqu'il est vrai, le nom et la version de Aspose.Words sont intégrés dans les fichiers produits. La valeur par défaut est **vrai** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [ImageSavingCallback](../../aspose.words.saving/xamlflowsaveoptions/imagesavingcallback) { get; set; } | Permet de contrôler la manière dont les images sont enregistrées lorsqu'un document est enregistré en XAML. |
| [ImagesFolder](../../aspose.words.saving/xamlflowsaveoptions/imagesfolder) { get; set; } | Spécifie le dossier physique dans lequel les images sont enregistrées lors de l'exportation d'un document au format XAML. La valeur par défaut est une chaîne vide. |
| [ImagesFolderAlias](../../aspose.words.saving/xamlflowsaveoptions/imagesfolderalias) { get; set; } | Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document XAML. La valeur par défaut est une chaîne vide. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| override [SaveFormat](../../aspose.words.saving/xamlflowsaveoptions/saveformat) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreXamlFlow . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

### Exemples

Montre comment imprimer les noms de fichiers des images liées créées lors de la conversion d'un document en flux .xaml.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Crée un objet "XamlFlowSaveOptions", que nous pouvons passer à la méthode "Save" du document
    // pour modifier la façon dont nous enregistrons le document au format d'enregistrement XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Utilisez la propriété "ImagesFolder" pour affecter un dossier dans le système de fichiers local dans lequel
    // Aspose.Words enregistrera toutes les images liées du document.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Utilisez la propriété "ImagesFolderAlias" pour utiliser ce dossier
    // lors de la construction d'URI d'image au lieu du nom du dossier d'images.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Un dossier spécifié par "ImagesFolderAlias" devra contenir les ressources au lieu de "ImagesFolder".
    // Nous devons nous assurer que le dossier existe avant que les flux du rappel puissent y mettre leurs ressources.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// Compte et imprime les noms de fichiers des images pendant que leur document parent est converti en flux de forme .xaml.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // Si nous avons spécifié un alias de dossier d'image, nous aurions également besoin
        // pour rediriger chaque flux pour mettre son image dans le dossier alias.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Voir également

* class [SaveOptions](../saveoptions)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
