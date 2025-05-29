---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.PdfSaveOptions pour optimiser l'enregistrement de vos documents. Personnalisez les paramètres pour une qualité et des performances de sortie PDF optimales.
type: docs
weight: 6320
url: /fr/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans lePdf format.

Pour en savoir plus, visitez le[Spécifier les options d'enregistrement](https://docs.aspose.com/words/net/specify-save-options/) article de documentation.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans le Pdf format. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | Un indicateur spécifiant s'il faut écrire ou non des opérateurs de positionnement de texte supplémentaires. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est`FAUX` . |
| [AttachmentsEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les pièces jointes sont intégrées au document PDF. |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non mettre en cache les graphiques placés en arrière-plan du document. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les couleurs sont rendues. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Spécifie le niveau de conformité aux normes PDF pour les documents de sortie. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Spécifie s'il faut convertir les références de notes de bas de page/de fin de texte dans l'article principal en hyperliens actifs. Lorsqu'il est cliqué, l'hyperlien mènera à la note de bas de page/de fin correspondante. La valeur par défaut est`FAUX` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Obtient ou définit une valeur déterminant la manière[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) sont exportés vers un fichier PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est**chaîne vide** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Obtient ou définit les détails pour la signature du document PDF de sortie. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | Un indicateur spécifiant si la barre de titre de la fenêtre doit afficher le titre du document tiré de l'entrée Titre du dictionnaire d'informations du document. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les effets 3D sont rendus. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les formes DrawingML sont rendues. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Permet de spécifier les options de sous-échantillonnage. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Contrôle la manière dont les polices sont intégrées dans les documents PDF résultants. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Obtient ou définit les détails de cryptage du document PDF de sortie. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non exporter la structure du document. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quand`vrai` , provoque l'intégration du nom et de la version d'Aspose.Words dans les fichiers produits. La valeur par défaut est`vrai` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non créer une balise « Span » dans la structure du document pour exporter la langue du texte. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | Obtient ou définit une valeur déterminant si un graphique de paragraphe doit être marqué comme un artefact. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Spécifie le mode d'incorporation de la police. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Détermine comment les signets dans les en-têtes/pieds de page sont exportés. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Spécifie comment l'espace colorimétrique sera sélectionné pour les images dans le document PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Spécifie le type de compression à utiliser pour toutes les images du document. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les objets d'encre (InkML) sont rendus. |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | Un indicateur indiquant si l'interpolation d'image doit être effectuée par un lecteur conforme. Lorsque`FAUX` est spécifié, l'indicateur n'est pas écrit dans le document de sortie et le comportement par défaut du lecteur est utilisé à la place. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit une valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est`FAUX` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Permet de spécifier les options de rendu du métafichier. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtient ou définit[`NumeralFormat`](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Obtient ou définit une valeur déterminant si les hyperliens dans le document PDF de sortie doivent être forcés à être ouverts dans une nouvelle fenêtre (ou onglet) d'un navigateur. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | L'indicateur indique s'il est nécessaire d'optimiser la sortie. Si cet indicateur est défini, les canevas imbriqués redondants et les canevas vides sont supprimés, les glyphes voisins avec le même formatage sont également concaténés. Remarque : la précision de l'affichage du contenu peut être affectée si cette propriété est définie sur`vrai` . La valeur par défaut est`FAUX` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Permet de spécifier les options de contour. |
| [PageLayout](../../aspose.words.saving/pdfsaveoptions/pagelayout/) { get; set; } | Spécifie la mise en page à utiliser lorsque le document est ouvert dans un lecteur PDF. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans un lecteur PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permet de contrôler la manière dont les pages séparées sont enregistrées lorsqu'un document est exporté vers un format de page fixe. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtient ou définit les pages à restituer. La valeur par défaut est toutes les pages du document. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non pré-mélanger les images transparentes avec une couleur d'arrière-plan noire. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Spécifie s'il faut conserver les champs de formulaire Microsoft Word en tant que champs de formulaire dans un PDF ou les convertir en texte. La valeur par défaut est`FAUX` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , joli format de sortie le cas échéant. La valeur par défaut est`FAUX` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| [RenderChoiceFormFieldBorder](../../aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/) { get; set; } | Spécifie s'il faut restituer la bordure du champ de formulaire de choix PDF. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtrePdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Spécifie le type de compression à utiliser pour tout le contenu textuel du document. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est`FAUX` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est`vrai` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré à l'aide d'une mise en page d'impression de livret, si elle est spécifiée via[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non remplacer les polices TrueType Arial, Times New Roman, Courier New et Symbol par les polices PDF Type 1 de base. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |
| [UseSdtTagAsFormFieldName](../../aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/) { get; set; } | Spécifie s'il faut utiliser la balise de contrôle SDT ou la propriété Id comme nom de champ de formulaire dans le PDF. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Obtient ou définit une valeur déterminant le type de zoom à appliquer lorsqu'un document est ouvert avec une visionneuse PDF. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Obtient ou définit une valeur déterminant le facteur de zoom (en pourcentage) pour un document. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Crée un clone profond de cet objet. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

## Exemples

Montre comment modifier la couleur de l'image avec la propriété des options d'enregistrement.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
// Définissez la propriété « ColorMode » sur « Niveaux de gris » pour rendre toutes les images du document en noir et blanc.
// La taille du document de sortie peut être plus grande avec ce paramètre.
// Définissez la propriété « ColorMode » sur « Normal » pour restituer toutes les images en couleur.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Montre comment appliquer la compression de texte lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « TextCompression » sur « PdfTextCompression.None » pour ne pas appliquer
// compression en texte lorsque nous enregistrons le document au format PDF.
// Définissez la propriété « TextCompression » sur « PdfTextCompression.Flate » pour appliquer la compression ZIP
// au texte lors de l'enregistrement du document au format PDF. Plus le document est volumineux, plus l'impact sera important.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Montre comment convertir un document entier en PDF avec trois niveaux dans le plan du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer les titres des niveaux 1 à 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Le document PDF de sortie contiendra un plan, qui est une table des matières répertoriant les titres dans le corps du document.
// Cliquer sur une entrée dans ce plan nous amènera à l'emplacement de son titre respectif.
// Définissez la propriété « HeadingsOutlineLevels » sur « 4 » pour exclure tous les titres dont les niveaux sont supérieurs à 4 du plan.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si une entrée de plan comporte des entrées ultérieures d'un niveau supérieur entre elle-même et l'entrée suivante du même niveau ou d'un niveau inférieur,
// Une flèche apparaîtra à gauche de l'entrée. Cette entrée est le « propriétaire » de plusieurs « sous-entrées ».
// Dans notre document, les entrées de plan du 5ème niveau de titre sont des sous-entrées de la deuxième entrée de plan du 4ème niveau,
// les entrées de niveau 4 et 5 sont des sous-entrées de la deuxième entrée de niveau 3, et ainsi de suite.
// Dans le plan, nous pouvons cliquer sur la flèche de l'entrée « propriétaire » pour réduire/développer toutes ses sous-entrées.
// Définissez la propriété « ExpandedOutlineLevels » sur « 2 » pour développer automatiquement toutes les entrées de plan de niveau 2 et inférieur
// et réduire toutes les entrées de niveau 3 et supérieur lorsque nous ouvrons le document.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Voir également

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
