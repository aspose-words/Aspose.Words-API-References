---
title: TxtSaveOptionsBase
second_title: Référence de l'API Aspose.Words pour .NET
description: La classe de base pour spécifier des options supplémentaires lors de lenregistrement dun document dans un format texte.
type: docs
weight: 5390
url: /fr/net/aspose.words.saving/txtsaveoptionsbase/
---
## TxtSaveOptionsBase class

La classe de base pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans un format texte.

```csharp
public abstract class TxtSaveOptionsBase : SaveOptions
```

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
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Permet de spécifier si les sauts de page doivent être conservés lors de l'export. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Spécifie la chaîne à utiliser comme saut de paragraphe lors de l'exportation au format texte. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

### Exemples

Montre comment enregistrer un document .txt avec un saut de paragraphe personnalisé.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Crée un objet "TxtSaveOptions", que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Définissez le "ParagraphBreak" sur une valeur personnalisée que nous souhaitons mettre à la fin de chaque paragraphe.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Voir également

* class [SaveOptions](../saveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
