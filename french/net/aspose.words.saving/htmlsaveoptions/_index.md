---
title: HtmlSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Peut être utilisé pour spécifier des options supplémentaires lors de lenregistrement dun document dans leHtml  Mhtml ouEpub format.
type: docs
weight: 4850
url: /fr/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leHtml , Mhtml ouEpub format.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions#constructor)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leHtml format. |
| [HtmlSaveOptions](htmlsaveoptions#constructor_1)(SaveFormat) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leHtml ,Mhtml ouEpub format. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **faux** . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent) { get; set; } | Spécifie si les retraits négatifs à gauche et à droite des paragraphes sont normalisés lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix) { get; set; } | Spécifie un préfixe qui est ajouté à tous les noms de classe CSS. La valeur par défaut est une chaîne vide et les noms de classe CSS générés n'ont pas de préfixe commun. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback) { get; set; } | Permet de contrôler la manière dont les styles CSS sont enregistrés lorsqu'un document est enregistré au format HTML, MHTML ou EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename) { get; set; } | Spécifie le chemin et le nom du fichier de feuille de style en cascade (CSS) écrit lorsqu'un document est exporté au format HTML. La valeur par défaut est une chaîne vide. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype) { get; set; } | Spécifie comment les styles CSS (Cascading Style Sheet) sont exportés vers HTML, MHTML ou EPUB. La valeur par défaut estInline pour HTML/MHTML et External pour EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des formes DrawingML. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback) { get; set; } | Permet de contrôler la manière dont les parties du document sont enregistrées lorsqu'un document est enregistré au format HTML ou EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria) { get; set; } | Spécifie comment le document doit être divisé lors de l'enregistrement dansHtml ouEpub format. La valeur par défaut estNone pour HTML et HeadingParagraph pour EPUB. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel) { get; set; } | Spécifie le niveau maximal d'en-têtes auquel diviser le document. La valeur par défaut est`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding) { get; set; } | Spécifie l'encodage à utiliser lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est`nouveau codage UTF8 (faux)` (UTF-8 sans nomenclature). |
| [EpubNavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel) { get; set; } | Spécifie le niveau maximal d'en-têtes remplis dans la carte de navigation lors de l'exportation au format IDPF EPUB. La valeur par défaut est`3` . |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources) { get; set; } | Spécifie s'il faut utiliser les URL CID (Content-ID) pour référencer les ressources (images, polices, CSS) incluses dans les documents MHTML . La valeur par défaut est`faux` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties) { get; set; } | Spécifie s'il faut exporter les propriétés de document intégrées et personnalisées vers HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext) { get; set; } | Contrôle la manière dont les champs de formulaire déroulants sont enregistrés au format HTML ou MHTML. La valeur par défaut est`faux` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources) { get; set; } | Spécifie si les ressources de police doivent être exportées vers HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64) { get; set; } | Spécifie si les ressources de polices doivent être intégrées au HTML dans l'encodage Base64. La valeur par défaut est`faux` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Lorsqu'il est vrai, le nom et la version de Aspose.Words sont intégrés dans les fichiers produits. La valeur par défaut est **vrai** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode) { get; set; } | Spécifie comment les en-têtes et pieds de page sont sortis en HTML, MHTML ou EPUB. La valeur par défaut estPerSection pour HTML/MHTML etNone pour EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64) { get; set; } | Spécifie si les images sont enregistrées au format Base64 dans la sortie HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation) { get; set; } | Spécifie si les informations de langue sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels) { get; set; } | Contrôle la façon dont les étiquettes de liste sont sorties au format HTML, MHTML ou EPUB. La valeur par défaut estAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages) { get; set; } | Spécifie si l'URL d'origine doit être utilisée comme URL des images liées. La valeur par défaut est`faux` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins) { get; set; } | Spécifie si les marges de la page sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup) { get; set; } | Spécifie si la mise en page est exportée vers HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize) { get; set; } | Spécifie si les tailles de police doivent être sorties en unités relatives lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation) { get; set; } | Spécifie s'il faut écrire les informations d'aller-retour lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`vrai` pour HTML et`faux` pour MHTML et EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg) { get; set; } | Contrôle si[`Shape`](../../aspose.words.drawing/shape) les nœuds sont convertis en images SVG lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`faux` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext) { get; set; } | Contrôle la manière dont les champs du formulaire de saisie de texte sont enregistrés au format HTML ou MHTML. La valeur par défaut est`faux` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers) { get; set; } | Spécifie s'il faut écrire les numéros de page dans la table des matières lors de l'enregistrement HTML, MHTML et EPUB. La valeur par défaut est`faux` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional) { get; set; } | Spécifie s'il faut écrire la déclaration DOCTYPE lors de l'enregistrement au format HTML ou MHTML. Lorsque`vrai` , écrit une déclaration DOCTYPE dans le document avant l'élément racine. La valeur par défaut est`faux`. Lors de l'enregistrement au format EPUB ou HTML5 (Html5 ) la déclaration DOCTYPE est toujours écrite. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold) { get; set; } | Contrôle les ressources de police qui nécessitent un sous-ensemble lors de l'enregistrement au format HTML, MHTML ou EPUB. La valeur par défaut est`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback) { get; set; } | Permet de contrôler la manière dont les polices sont enregistrées lorsqu'un document est enregistré au format HTML, MHTML ou EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder) { get; set; } | Spécifie le dossier physique dans lequel les polices sont enregistrées lors de l'exportation d'un document au format HTML. La valeur par défaut est une chaîne vide. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias) { get; set; } | Spécifie le nom du dossier utilisé pour construire les URI des polices écrites dans un document HTML. La valeur par défaut est une chaîne vide. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion) { get; set; } | Spécifie la version de la norme HTML qui doit être utilisée lors de l'enregistrement du document au format HTML ou MHTML. La valeur par défaut estXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution) { get; set; } | Spécifie la résolution de sortie des images lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est`96 ppp` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback) { get; set; } | Permet de contrôler la manière dont les images sont enregistrées lorsqu'un document est enregistré au format HTML, MHTML ou EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder) { get; set; } | Spécifie le dossier physique dans lequel les images sont enregistrées lors de l'exportation d'un document au format HTML. La valeur par défaut est une chaîne vide. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias) { get; set; } | Spécifie le nom du dossier utilisé pour construire les URI d'image écrites dans un document HTML. La valeur par défaut est une chaîne vide. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat) { get; set; } | Spécifie dans quel format les métafichiers sont enregistrés lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut estPng , ce qui signifie que les métafichiers sont rendus en images PNG raster. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode) { get; set; } | Contrôle la façon dont les objets OfficeMath sont exportés vers HTML, MHTML ou EPUB. La valeur par défaut est`HtmlOfficeMathOutputMode.Image` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames) { get; set; } | Spécifie si les noms de famille de polices utilisés dans le document sont résolus et remplacés selon [`FontSettings`](../../aspose.words/document/fontsettings) lors de l'écriture dans des formats basés sur HTML. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder) { get; set; } | Spécifie un dossier physique dans lequel toutes les ressources telles que les images, les polices et les CSS externes sont enregistrées lorsqu'un document est exporté au format HTML. La valeur par défaut est une chaîne vide. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias) { get; set; } | Spécifie le nom du dossier utilisé pour construire les URI de toutes les ressources écrites dans un document HTML. La valeur par défaut est une chaîne vide. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut êtreHtml ,Mhtml ouEpub . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize) { get; set; } | Spécifie si les images sont mises à l'échelle par Aspose.Words à la taille de la forme de délimitation lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est`vrai` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode) { get; set; } | Contrôle la manière dont les largeurs de tableau, de ligne et de cellule sont exportées vers HTML, MHTML ou EPUB. La valeur par défaut estAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

### Exemples

Montre comment spécifier le dossier de stockage des images liées après l'enregistrement au format .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Définissez une option pour exporter les champs de formulaire en tant que texte brut au lieu d'éléments d'entrée HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Montre comment utiliser un encodage spécifique lors de l'enregistrement d'un document au format .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilisez un objet SaveOptions pour spécifier l'encodage d'un document que nous allons enregistrer.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Par défaut, un document de sortie .epub aura tout son contenu dans une seule partie HTML.
// Un critère de découpage permet de segmenter le document en plusieurs parties HTML.
// Nous allons définir les critères pour diviser le document en paragraphes d'en-tête.
// Ceci est utile pour les lecteurs qui ne peuvent pas lire les fichiers HTML plus importants qu'une taille spécifique.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Spécifiez que nous voulons exporter les propriétés du document.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Montre comment diviser un document en plusieurs parties et les enregistrer.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crée un objet "HtmlFixedSaveOptions", que nous pouvons passer à la méthode "Save" du document
    // pour modifier la façon dont nous convertissons le document en HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si nous enregistrons le document normalement, il y aura une sortie HTML
    // document avec tout le contenu du document source.
    // Définissez la propriété "DocumentSplitCriteria" sur "DocumentSplitCriteria.SectionBreak" pour
    // enregistre notre document dans plusieurs fichiers HTML : un pour chaque section.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Attribuez un rappel personnalisé à la propriété "DocumentPartSavingCallback" pour modifier la logique d'enregistrement de la partie du document.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si nous convertissons un document contenant des images en html, nous nous retrouverons avec un fichier html qui renvoie à plusieurs images.
    // Chaque image sera sous la forme d'un fichier dans le système de fichiers local.
    // Il existe également un rappel qui peut personnaliser le nom et l'emplacement du système de fichiers de chaque image.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Définit des noms de fichiers personnalisés pour les documents de sortie dans lesquels l'opération d'enregistrement divise un document.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Nous pouvons accéder à l'intégralité du document source via la propriété "Document".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Vous trouverez ci-dessous deux manières de spécifier où Aspose.Words enregistrera chaque partie du document.
        // 1 - Définissez un nom de fichier pour le fichier partiel de sortie :
        args.DocumentPartFileName = partFileName;

        // 2 - Créez un flux personnalisé pour le fichier partiel de sortie :
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Définit des noms de fichiers personnalisés pour les fichiers image créés par une conversion HTML.
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

        // Vous trouverez ci-dessous deux manières de spécifier où Aspose.Words enregistrera chaque partie du document.
        // 1 - Définissez un nom de fichier pour le fichier image de sortie :
        args.ImageFileName = imageFileName;

        // 2 - Créez un flux personnalisé pour le fichier image de sortie :
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

* class [SaveOptions](../saveoptions)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
