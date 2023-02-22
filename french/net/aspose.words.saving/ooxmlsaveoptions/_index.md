---
title: Class OoxmlSaveOptions
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.OoxmlSaveOptions classe. Peut être utilisé pour spécifier des options supplémentaires lors de lenregistrement dun document dans leDocx  Docm Dotx Dotm ou FlatOpc format.
type: docs
weight: 5070
url: /fr/net/aspose.words.saving/ooxmlsaveoptions/
---
## OoxmlSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leDocx , Docm ,Dotx ,Dotm ou FlatOpc format.

```csharp
public class OoxmlSaveOptions : SaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [OoxmlSaveOptions](ooxmlsaveoptions/#constructor)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leDocx format. |
| [OoxmlSaveOptions](ooxmlsaveoptions/#constructor_1)(SaveFormat) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leDocx , Docm ,Dotx ,Dotm ou FlatOpc format. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est **faux** . |
| [Compliance](../../aspose.words.saving/ooxmlsaveoptions/compliance/) { get; set; } | Spécifie la version OOXML du document de sortie. La valeur par défaut estEcma376_2006 . |
| [CompressionLevel](../../aspose.words.saving/ooxmlsaveoptions/compressionlevel/) { get; set; } | Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut estNormal . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est **chaîne vide** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des effets DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des formes DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Lorsqu'il est vrai, le nom et la version de Aspose.Words sont intégrés dans les fichiers produits. La valeur par défaut est **vrai** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Obtient ou définit la valeur déterminant quels formats de document sont autorisés à être mappés par[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Par défaut uniquementFlatOpc le format de document est autorisé à être mappé. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML). |
| [KeepLegacyControlChars](../../aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/) { get; set; } | Conserve la représentation originale des caractères de contrôle hérités. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** . |
| [Password](../../aspose.words.saving/ooxmlsaveoptions/password/) { get; set; } | Obtient/définit un mot de passe pour chiffrer le document à l'aide de l'algorithme de chiffrement standard ECMA376. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , jolis formats de sortie le cas échéant. La valeur par défaut est **faux** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| override [SaveFormat](../../aspose.words.saving/ooxmlsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut êtreDocx ,Docm , Dotx ,Dotm ouFlatOpc . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier des fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est false ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est **vrai** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Obtient ou définit la valeur déterminant si le contenu de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) est mis à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

### Exemples

Montre comment définir une spécification de conformité OOXML pour un document enregistré à respecter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous configurons les options de compatibilité pour se conformer à Microsoft Word 2003,
// l'insertion d'une image définira sa forme à l'aide de VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// La norme OOXML "ISO/IEC 29500:2008" ne prend pas en charge les formes VML.
// Si nous définissons la propriété "Compliance" de l'objet SaveOptions sur "OoxmlCompliance.Iso29500_2008_Strict",
 // tout document que nous enregistrons en passant cet objet devra suivre cette norme.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme à l'aide de DML pour respecter la norme OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Voir également

* class [SaveOptions](../saveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


