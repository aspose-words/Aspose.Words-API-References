---
title: Class MarkdownSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.MarkdownSaveOptions classe. Classe pour spécifier des options supplémentaires lors de lenregistrement dun document dans leMarkdown format.
type: docs
weight: 5000
url: /fr/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

Classe pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leMarkdown format.

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
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **faux** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des formes DrawingML. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Spécifie l'encodage à utiliser lors de l'exportation au format texte. La valeur par défaut est **Encodage.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Lorsqu'il est vrai, le nom et la version de Aspose.Words sont intégrés dans les fichiers produits. La valeur par défaut est **vrai** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Spécifie la façon dont les en-têtes et les pieds de page sont exportés vers les formats de texte. La valeur par défaut estPrimaryOnly . |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | Spécifie si les images sont enregistrées au format Base64 dans le fichier de sortie. La valeur par défaut est`faux` . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Permet de spécifier si les sauts de page doivent être conservés lors de l'export. |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | Permet de contrôler la manière dont les images sont enregistrées lorsqu'un document est enregistré dans Markdown format. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | Spécifie le dossier physique dans lequel les images sont enregistrées lors de l'exportation d'un document vers leMarkdown format. La valeur par défaut est une chaîne vide. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Spécifie la chaîne à utiliser comme saut de paragraphe lors de l'exportation au format texte. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreMarkdown . |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | Obtient ou définit une valeur qui spécifie comment aligner le contenu des tables lors de l'exportation vers leMarkdown format. La valeur par défaut estAuto . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

### Voir également

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


