---
title: Class XamlFixedSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.XamlFixedSaveOptions classe. Peut être utilisé pour spécifier des options supplémentaires lors de lenregistrement dun document dans leXamlFixed format.
type: docs
weight: 5410
url: /fr/net/aspose.words.saving/xamlfixedsaveoptions/
---
## XamlFixedSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leXamlFixed format.

```csharp
public class XamlFixedSaveOptions : FixedPageSaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [XamlFixedSaveOptions](xamlfixedsaveoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **faux** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des couleurs. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des formes DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Lorsqu'il est vrai, le nom et la version de Aspose.Words sont intégrés dans les fichiers produits. La valeur par défaut est **vrai** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document HTML. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Permet de spécifier les options de rendu des métafichiers. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtient ou définit[`NumeralFormat`](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Indicateur indique s'il est nécessaire d'optimiser la sortie. Si cet indicateur est défini, les canevas imbriqués redondants et les canevas vides sont supprimés, également les glyphes voisins avec le même formatage sont concaténés. Remarque : La précision de l'affichage du contenu peut être affectée si cette propriété est définie sur true. La valeur par défaut est false. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permet de contrôler la manière dont les pages séparées sont enregistrées lorsqu'un document est exporté au format de page fixe. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtient ou définit les pages à afficher. La valeur par défaut est toutes les pages du document. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| [ResourceSavingCallback](../../aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Permet de contrôler la manière dont les ressources (images et polices) sont enregistrées lorsqu'un document est exporté au format Xaml à page fixe. |
| [ResourcesFolder](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/) { get; set; } | Spécifie le dossier physique dans lequel les ressources (images et polices) sont enregistrées lors de l'exportation d'un document au format Xaml à page fixe. La valeur par défaut est`nul` . |
| [ResourcesFolderAlias](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document Xaml à page fixe. La valeur par défaut est`nul` . |
| override [SaveFormat](../../aspose.words.saving/xamlfixedsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreXamlFixed . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

### Exemples

Montre comment imprimer les URI des ressources liées créées lors de la conversion d'un document en .xaml de forme fixe.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Crée un objet "XamlFixedSaveOptions", que nous pouvons passer à la méthode "Save" du document
    // pour modifier la façon dont nous enregistrons le document au format d'enregistrement XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilisez la propriété "ResourcesFolder" pour affecter un dossier dans le système de fichiers local dans lequel
    // Aspose.Words enregistrera toutes les ressources liées du document, telles que les images et les polices.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Utilisez la propriété "ResourcesFolderAlias" pour utiliser ce dossier
    // lors de la construction d'URI d'image au lieu du nom du dossier de ressources.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Un dossier spécifié par "ResourcesFolderAlias" devra contenir les ressources au lieu de "ResourcesFolder".
    // Nous devons nous assurer que le dossier existe avant que les flux du rappel puissent y mettre leurs ressources.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Compte et imprime les URI des ressources créées lors de la conversion en .xaml fixe.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // Si nous avons spécifié un alias de dossier de ressources, nous aurions également besoin
        // pour rediriger chaque flux pour mettre sa ressource dans le dossier alias.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Voir également

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


