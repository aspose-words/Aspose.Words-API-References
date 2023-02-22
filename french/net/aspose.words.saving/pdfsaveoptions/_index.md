---
title: Class PdfSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.PdfSaveOptions classe. Peut être utilisé pour spécifier des options supplémentaires lors de lenregistrement dun document dans lePdf format.
type: docs
weight: 5240
url: /fr/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans lePdf format.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans the Pdf format. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | Un indicateur spécifiant s'il faut ou non écrire des opérateurs de positionnement de texte supplémentaires. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **faux** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des couleurs. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Spécifie le niveau de conformité aux normes PDF pour les documents de sortie. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Spécifie s'il faut convertir les références de note de bas de page/note de fin dans l'histoire du texte principal en hyperliens actifs. Lorsque vous cliquez dessus, l'hyperlien mènera à la note de bas de page/note de fin correspondante. La valeur par défaut est`faux` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Obtient ou définit une valeur déterminant la manière[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) sont exportés vers un fichier PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Obtient ou définit les détails de signature du document PDF de sortie. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | Un indicateur spécifiant si la barre de titre de la fenêtre doit afficher le titre du document extrait de l'entrée Titre du dictionnaire d'informations sur le document. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets 3D. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des formes DrawingML. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Permet de spécifier les options de sous-échantillonnage. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Contrôle la manière dont les polices sont intégrées dans les documents PDF résultants. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Obtient ou définit les détails de cryptage du document PDF de sortie. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non exporter la structure du document. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Lorsqu'il est vrai, le nom et la version de Aspose.Words sont intégrés dans les fichiers produits. La valeur par défaut est **vrai** . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non créer une balise "Span" dans la structure du document pour exporter la langue du texte. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Spécifie le mode d'incorporation des polices. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Détermine comment les signets dans les en-têtes/pieds de page sont exportés. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Spécifie comment l'espace colorimétrique sera sélectionné pour les images dans le document PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Spécifie le type de compression à utiliser pour toutes les images du document. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | Un indicateur indiquant si l'interpolation d'image doit être effectuée par un lecteur conforme. Lorsque`faux` est spécifié, l'indicateur n'est pas écrit dans le document de sortie et le comportement par défaut du lecteur est utilisé à la place. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Obtient ou définit une valeur déterminant la qualité des images JPEG dans le document PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Permet de spécifier les options de rendu des métafichiers. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Obtient ou définit[`NumeralFormat`](../numeralformat/) utilisé pour le rendu des chiffres. Les chiffres européens sont utilisés par défaut. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Obtient ou définit une valeur déterminant si les hyperliens dans le document PDF de sortie sont forcés à s'ouvrir dans une nouvelle fenêtre (ou onglet) d'un navigateur. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Indicateur indique s'il est nécessaire d'optimiser la sortie. Si cet indicateur est défini, les canevas imbriqués redondants et les canevas vides sont supprimés, également les glyphes voisins avec le même formatage sont concaténés. Remarque : La précision de l'affichage du contenu peut être affectée si cette propriété est définie sur true. La valeur par défaut est false. |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Permet de spécifier les options de contour. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans le lecteur PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permet de contrôler la manière dont les pages séparées sont enregistrées lorsqu'un document est exporté au format de page fixe. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtient ou définit les pages à afficher. La valeur par défaut est toutes les pages du document. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non pré-mélanger les images transparentes avec une couleur d'arrière-plan noire. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Spécifie s'il faut conserver les champs de formulaire Microsoft Word en tant que champs de formulaire dans le PDF ou les convertir en texte. La valeur par défaut est`faux` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtrePdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Spécifie le type de compression à utiliser pour tout le contenu textuel du document. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d'impression de livret, si elle est spécifiée via[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non remplacer les polices TrueType Arial, Times New Roman, Courier New et Symbol par les polices de base PDF Type 1. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Obtient ou définit une valeur déterminant le type de zoom à appliquer lorsqu'un document est ouvert avec une visionneuse PDF. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Obtient ou définit une valeur déterminant le facteur de zoom (en pourcentage) pour un document. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Crée un clone profond de cet objet. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

### Exemples

Montre comment changer la couleur de l'image avec la propriété des options d'enregistrement.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
// Définissez la propriété "ColorMode" sur "Grayscale" pour rendre toutes les images du document en noir et blanc.
// La taille du document de sortie peut être plus grande avec ce paramètre.
// Définissez la propriété "ColorMode" sur "Normal" pour rendre toutes les images en couleur.
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

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "TextCompression" sur "PdfTextCompression.None" pour ne rien appliquer
// compression en texte lorsque nous enregistrons le document au format PDF.
// Définissez la propriété "TextCompression" sur "PdfTextCompression.Flate" pour appliquer la compression ZIP
// au texte lorsque nous enregistrons le document au format PDF. Plus le document est volumineux, plus l'impact que cela aura sera grand.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Montre comment convertir un document entier en PDF avec trois niveaux dans le plan du document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère les titres des niveaux 1 à 5.
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

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Le document PDF de sortie contiendra un plan, qui est une table des matières qui répertorie les en-têtes dans le corps du document.
// Cliquer sur une entrée dans ce plan nous amènera à l'emplacement de son en-tête respectif.
// Définissez la propriété "HeadingsOutlineLevels" sur "4" pour exclure tous les titres dont les niveaux sont supérieurs à 4 du plan.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Si une entrée de plan comporte des entrées ultérieures d'un niveau supérieur entre elle-même et l'entrée suivante du même niveau ou d'un niveau inférieur,
// une flèche apparaîtra à gauche de l'entrée. Cette entrée est le "propriétaire" de plusieurs de ces "sous-entrées".
// Dans notre document, les entrées de plan du 5ème niveau de titre sont des sous-entrées de la deuxième entrée de plan de 4ème niveau,
 // les entrées de niveau 4 et 5 sont des sous-entrées de la deuxième entrée de niveau 3, et ainsi de suite.
// Dans l'outline, on peut cliquer sur la flèche de l'entrée "propriétaire" pour réduire/développer toutes ses sous-entrées.
// Définissez la propriété "ExpandedOutlineLevels" sur "2" pour développer automatiquement toutes les entrées de plan de niveau 2 et inférieur
 // et réduire toutes les entrées de niveau et 3 et plus lorsque nous ouvrons le document.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Voir également

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


