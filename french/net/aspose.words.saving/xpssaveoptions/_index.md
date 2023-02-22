---
title: Class XpsSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.XpsSaveOptions classe. Peut être utilisé pour spécifier des options supplémentaires lors de lenregistrement dun document dans leXps format.
type: docs
weight: 5430
url: /fr/net/aspose.words.saving/xpssaveoptions/
---
## XpsSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leXps format.

```csharp
public class XpsSaveOptions : FixedPageSaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [XpsSaveOptions](xpssaveoptions/#constructor)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leXps format. |
| [XpsSaveOptions](xpssaveoptions/#constructor_1)(SaveFormat) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leXps ouOpenXps format. |

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
| [OutlineOptions](../../aspose.words.saving/xpssaveoptions/outlineoptions/) { get; } | Permet de spécifier les options de contour. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Permet de contrôler la manière dont les pages séparées sont enregistrées lorsqu'un document est exporté au format de page fixe. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Obtient ou définit les pages à afficher. La valeur par défaut est toutes les pages du document. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| override [SaveFormat](../../aspose.words.saving/xpssaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreXps . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/) { get; set; } | Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré en utilisant une mise en page d'impression de livret, si elle est spécifiée via[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |

### Exemples

Montre comment limiter le niveau des titres qui apparaîtront dans le plan d'un document XPS enregistré.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer des en-têtes pouvant servir d'entrées de table des matières des niveaux 1, 2, puis 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crée un objet "XpsSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Le document XPS de sortie contiendra un plan, une table des matières qui répertorie les en-têtes dans le corps du document.
// Cliquer sur une entrée dans ce plan nous amènera à l'emplacement de son en-tête respectif.
// Définissez la propriété "HeadingsOutlineLevels" sur "2" pour exclure tous les titres dont les niveaux sont supérieurs à 2 du plan.
// Les deux derniers titres que nous avons insérés ci-dessus n'apparaîtront pas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Voir également

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


