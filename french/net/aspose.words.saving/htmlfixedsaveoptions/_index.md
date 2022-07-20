---
title: HtmlFixedSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Peut être utilisé pour spécifier des options supplémentaires lors de lenregistrement dun document dans leHtmlFixed format.
type: docs
weight: 4820
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leHtmlFixed format.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **faux** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des couleurs. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix) { get; set; } | Spécifie le préfixe qui est ajouté à tous les noms de classe dans le fichier style.css. La valeur par défaut est`"aw"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des formes DrawingML. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding) { get; set; } | Spécifie l'encodage à utiliser lors de l'exportation vers HTML. La valeur par défaut est`nouveau codage UTF8 (vrai)` (UTF-8 avec nomenclature). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss) { get; set; } | Spécifie si le CSS (Cascading Style Sheet) doit être intégré dans le document Html. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts) { get; set; } | Spécifie si les polices doivent être intégrées dans le document HTML au format Base64. Notez que la définition de cet indicateur peut augmenter considérablement la taille du fichier HTML de sortie. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages) { get; set; } | Spécifie si les images doivent être intégrées dans le document HTML au format Base64. Notez que la définition de cet indicateur peut augmenter considérablement la taille du fichier HTML de sortie. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg) { get; set; } | Spécifie si les ressources SVG doivent être intégrées dans le document HTML. La valeur par défaut est`vrai` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields) { get; set; } | Obtient ou définit une indication indiquant si les champs de formulaire sont exportés en tant qu'éléments interactifs (en tant que balise 'input') plutôt que convertis en texte ou en graphiques. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Lorsqu'il est vrai, le nom et la version de Aspose.Words sont intégrés dans les fichiers produits. La valeur par défaut est **vrai** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat) { get; set; } | Obtient ou définit[`ExportFontFormat`](../exportfontformat) utilisé pour l'exportation de polices. La valeur par défaut estWoff . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality) { get; set; } | Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document HTML. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | Permet de spécifier les options de rendu des métafichiers. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | Obtient ou définit[`NumeralFormat`](../numeralformat) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput) { get; set; } | Indicateur indique s'il est nécessaire d'optimiser la sortie. Si cet indicateur est défini, les canevas imbriqués redondants et les canevas vides sont supprimés, également les glyphes voisins avec le même formatage sont concaténés. Remarque : La précision de l'affichage du contenu peut être affectée si cette propriété est définie sur true. La valeur par défaut est true. |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment) { get; set; } | Spécifie l'alignement horizontal des pages dans un document HTML. La valeur par défaut est`HtmlFixedHorizontalPageAlignment.Center` . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins) { get; set; } | Spécifie les marges autour des pages dans un document HTML. La valeur des marges est mesurée en points et doit être égale ou supérieure à 0. La valeur par défaut est de 10 points. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | Permet de contrôler la manière dont les pages séparées sont enregistrées lorsqu'un document est exporté au format de page fixe. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | Obtient ou définit les pages à afficher. La valeur par défaut est toutes les pages du document. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback) { get; set; } | Permet de contrôler la manière dont les ressources (images, polices et css) sont enregistrées lorsqu'un document est exporté au format Html à page fixe. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder) { get; set; } | Spécifie le dossier physique dans lequel les ressources (images, polices, css) sont enregistrées lors de l'exportation d'un document au format Html. La valeur par défaut est`nul` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias) { get; set; } | Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document HTML. La valeur par défaut est`nul` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately) { get; set; } | Flag indique si les règles CSS "@font-face" doivent être placées dans un fichier séparé "fontFaces.css" lorsqu'un document est enregistré avec une feuille de style externe (c'est-à-dire lorsque[`ExportEmbeddedCss`](./exportembeddedcss) est`faux` ). La valeur par défaut est`faux` , toutes les règles CSS sont écrites dans un seul fichier "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder) { get; set; } | Spécifie si la bordure autour des pages doit être affichée. La valeur par défaut est`vrai` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts) { get; set; } | L'indicateur indique si les polices de la machine cible doivent être utilisées pour afficher le document. Si cet indicateur est défini sur vrai,[`FontFormat`](./fontformat) et[`ExportEmbeddedFonts`](./exportembeddedfonts)les propriétés n'ont pas d'effet, également[`ResourceSavingCallback`](./resourcesavingcallback) n'est pas déclenché pour les polices. La valeur par défaut est false. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

### Exemples

Montre comment utiliser un rappel pour imprimer les URI des ressources externes créées lors de la conversion d'un document en HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // Un dossier spécifié par ResourcesFolderAlias contiendra les ressources au lieu de ResourcesFolder.
    // Nous devons nous assurer que le dossier existe avant que les flux puissent y mettre leurs ressources.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Compte et imprime les URI des ressources contenues par lorsqu'elles sont converties en HTML fixe.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Si nous définissons un alias de dossier dans l'objet SaveOptions, nous pourrons l'imprimer à partir d'ici.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Par défaut, 'ResourceFileUri' utilise le dossier système pour les polices.
                // Pour éviter des problèmes sur d'autres plates-formes, vous devez spécifier explicitement le chemin des polices.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Si nous avons spécifié un dossier dans la propriété "ResourcesFolderAlias",
        // nous devrons également rediriger chaque flux pour mettre sa ressource dans ce dossier.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Voir également

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
