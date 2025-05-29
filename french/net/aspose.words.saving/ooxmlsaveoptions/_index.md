---
title: OoxmlSaveOptions Class
linktitle: OoxmlSaveOptions
articleTitle: OoxmlSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.OoxmlSaveOptions pour améliorer l'enregistrement de documents aux formats Docx, Docm, Dotx, Dotm et FlatOpc avec des fonctionnalités personnalisables.
type: docs
weight: 6130
url: /fr/net/aspose.words.saving/ooxmlsaveoptions/
---
## OoxmlSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leDocx , Docm ,Dotx ,Dotm ou FlatOpc format.

Pour en savoir plus, visitez le[Spécifier les options d'enregistrement](https://docs.aspose.com/words/net/specify-save-options/) article de documentation.

```csharp
public class OoxmlSaveOptions : SaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [OoxmlSaveOptions](ooxmlsaveoptions/#constructor)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leDocx format. |
| [OoxmlSaveOptions](ooxmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leDocx , Docm ,Dotx ,Dotm ou FlatOpc format. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est`FAUX` . |
| [Compliance](../../aspose.words.saving/ooxmlsaveoptions/compliance/) { get; set; } | Spécifie la version OOXML du document de sortie. La valeur par défaut estEcma376_2006 . |
| [CompressionLevel](../../aspose.words.saving/ooxmlsaveoptions/compressionlevel/) { get; set; } | Spécifie le niveau de compression utilisé pour enregistrer le document. La valeur par défaut estNormal . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est**chaîne vide** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/ooxmlsaveoptions/digitalsignaturedetails/) { get; set; } | Obtient ou définit[`DigitalSignatureDetails`](../digitalsignaturedetails/) objet utilisé pour signer un document. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les effets 3D sont rendus. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les formes DrawingML sont rendues. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quand`vrai` , provoque l'intégration du nom et de la version d'Aspose.Words dans les fichiers produits. La valeur par défaut est`vrai` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les objets d'encre (InkML) sont rendus. |
| [KeepLegacyControlChars](../../aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/) { get; set; } | Conserve la représentation originale des caractères de contrôle hérités. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit une valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est`FAUX` . |
| [Password](../../aspose.words.saving/ooxmlsaveoptions/password/) { get; set; } | Obtient/définit un mot de passe pour crypter le document à l'aide de l'algorithme de cryptage standard ECMA376. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , joli format de sortie le cas échéant. La valeur par défaut est`FAUX` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| override [SaveFormat](../../aspose.words.saving/ooxmlsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut êtreDocx ,Docm , Dotx ,Dotm ouFlatOpc . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est`FAUX` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est`vrai` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |
| [Zip64Mode](../../aspose.words.saving/ooxmlsaveoptions/zip64mode/) { get; set; } | Spécifie s'il faut ou non utiliser les extensions de format ZIP64 pour le document de sortie. La valeur par défaut estNever . |

## Exemples

Montre comment définir une spécification de conformité OOXML à laquelle un document enregistré doit adhérer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous configurons les options de compatibilité pour être conformes à Microsoft Word 2003,
// l'insertion d'une image définira sa forme à l'aide de VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// La norme OOXML « ISO/IEC 29500:2008 » ne prend pas en charge les formes VML.
// Si nous définissons la propriété « Compliance » de l'objet SaveOptions sur « OoxmlCompliance.Iso29500_2008_Strict »,
 // tout document que nous sauvegardons en passant cet objet devra suivre cette norme.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme à l'aide de DML pour adhérer à la norme OOXML « ISO/IEC 29500:2008 ».
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Voir également

* class [SaveOptions](../saveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
