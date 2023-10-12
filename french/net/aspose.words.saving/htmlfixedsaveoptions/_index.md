---
title: Class HtmlFixedSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.HtmlFixedSaveOptions classe. Peut être utilisé pour spécifier des options supplémentaires lors de lenregistrement dun document dans leHtmlFixed format.
type: docs
weight: 5080
url: /fr/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leHtmlFixed format.

Pour en savoir plus, visitez le[Spécifier les options d'enregistrement](https://docs.aspose.com/words/net/specify-save-options/) article documentaire.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est`FAUX` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les couleurs sont rendues. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | Spécifie le préfixe qui est ajouté à tous les noms de classe dans le fichier style.css. La valeur par défaut est`"oh"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les effets 3D sont rendus. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la façon dont les effets DrawingML sont rendus. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la façon dont les formes DrawingML sont rendues. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | Spécifie l'encodage à utiliser lors de l'exportation au format HTML. La valeur par défaut est`nouveau codage UTF8 (vrai)` (UTF-8 avec nomenclature). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | Spécifie si le CSS (Cascading Style Sheet) doit être intégré dans le document HTML. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | Spécifie si les polices doivent être intégrées dans le document HTML au format Base64. Remarque : la définition de cet indicateur peut augmenter considérablement la taille du fichier HTML de sortie. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | Spécifie si les images doivent être intégrées dans un document HTML au format Base64. Remarque : la définition de cet indicateur peut augmenter considérablement la taille du fichier HTML de sortie. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | Spécifie si les ressources SVG doivent être intégrées dans le document HTML. La valeur par défaut est`vrai` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | Obtient ou définit une indication indiquant si les champs de formulaire sont exportés en tant qu'éléments interactifs (en tant que balise « entrée ») plutôt que convertis en texte ou en graphiques. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quand`vrai` , entraîne l'intégration du nom et de la version d'Aspose.Words dans les fichiers produits. La valeur par défaut est`vrai` . |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | Obtient ou définit[`ExportFontFormat`](../exportfontformat/) utilisé pour l'exportation de polices. La valeur par défaut estWoff . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les objets Ink (InkML) sont rendus. |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document HTML. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est`FAUX` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Permet de spécifier les options de rendu du métafichier. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtient ou définit[`NumeralFormat`](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | L'indicateur indique s'il est nécessaire d'optimiser la sortie. Si cet indicateur est défini, les canevas imbriqués redondants et les canevas vides sont supprimés, également les glyphes voisins avec le même formatage sont concaténés. Remarque : la précision de l'affichage du contenu peut être affectée si cette propriété est définie sur`vrai` . La valeur par défaut est`vrai` . |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | Spécifie l'alignement horizontal des pages dans un document HTML. La valeur par défaut estCenter . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | Spécifie les marges autour des pages d'un document HTML. La valeur des marges est mesurée en points et doit être égale ou supérieure à 0. La valeur par défaut est de 10 points. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permet de contrôler la façon dont les pages séparées sont enregistrées lorsqu'un document est exporté au format de page fixe. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtient ou définit les pages à restituer. La valeur par défaut est toutes les pages du document. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` jolis formats de sortie le cas échéant. La valeur par défaut est`FAUX` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Permet de contrôler la façon dont les ressources (images, polices et CSS) sont enregistrées lorsqu'un document est exporté au format HTML de page fixe. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | Spécifie le dossier physique dans lequel les ressources (images, polices, CSS) sont enregistrées lors de l'exportation d'un document au format HTML. La valeur par défaut est`nul` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Spécifie le nom du dossier utilisé pour construire les URI d'image écrits dans un document HTML. La valeur par défaut est`nul` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | L'indicateur indique si les règles CSS "@font-face" doivent être placées dans un fichier séparé "fontFaces.css" lorsqu'un document est enregistré avec une feuille de style externe (c'est-à-dire lorsqu'[`ExportEmbeddedCss`](./exportembeddedcss/) est`FAUX` ). La valeur par défaut est`FAUX` , toutes les règles CSS sont écrites dans un seul fichier "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options de sauvegarde est utilisé. Ne peut êtreHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | Spécifie si la bordure autour des pages doit être affichée. La valeur par défaut est`vrai` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier des fichiers temporaires utilisé lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est`FAUX` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est`vrai` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | L'indicateur indique si les polices de la machine cible doivent être utilisées pour afficher le document. Si cet indicateur est défini sur`vrai` ,[`FontFormat`](./fontformat/) et[`ExportEmbeddedFonts`](./exportembeddedfonts/) les propriétés n'ont pas d'effet, également[`ResourceSavingCallback`](./resourcesavingcallback/) n'est pas déclenché pour les polices. La valeur par défaut est`FAUX` . |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Détermine si l'objet spécifié a une valeur égale à l'objet actuel. |

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
    // Nous devons nous assurer que le dossier existe avant que les flux puissent y placer leurs ressources.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Compte et imprime les URI des ressources contenues par au fur et à mesure de leur conversion en HTML fixe.
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
                // Pour éviter des problèmes sur d'autres plateformes, vous devez spécifier explicitement le chemin des polices.
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

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


