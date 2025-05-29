---
title: OdtSaveOptions Class
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.OdtSaveOptions pour améliorer l'enregistrement de vos documents. Personnalisez les paramètres pour les formats ODT/OTT et optimisez votre flux de travail !
type: docs
weight: 6110
url: /fr/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Peut être utilisé pour spécifier des options supplémentaires lors de l'enregistrement d'un document dans leOdt ou Ott format.

Pour en savoir plus, visitez le[Spécifier les options d'enregistrement](https://docs.aspose.com/words/net/specify-save-options/) article de documentation.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions/#constructor)() | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leOdt format. |
| [OdtSaveOptions](odtsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leOdt ou Ott format. |
| [OdtSaveOptions](odtsaveoptions/#constructor_2)(*string*) | Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document dans leOdt format crypté avec un mot de passe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Obtient ou définit une valeur booléenne indiquant s'il faut autoriser l'incorporation de polices avec des contours PostScript lors de l'incorporation de polices TrueType dans un document lors de son enregistrement. La valeur par défaut est`FAUX` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Obtient ou définit le fuseau horaire local personnalisé utilisé pour les champs de date/heure. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Obtient ou définit le chemin d'accès au modèle par défaut (y compris le nom de fichier). La valeur par défaut de cette propriété est**chaîne vide** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/odtsaveoptions/digitalsignaturedetails/) { get; set; } | Obtient ou définit[`DigitalSignatureDetails`](../digitalsignaturedetails/) objet utilisé pour signer un document. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les effets 3D sont rendus. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les formes DrawingML sont rendues. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quand`vrai` , provoque l'intégration du nom et de la version d'Aspose.Words dans les fichiers produits. La valeur par défaut est`vrai` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Obtient ou définit une valeur déterminant la manière dont les objets d'encre (InkML) sont rendus. |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11/) { get; set; } | Spécifie si l'exportation doit correspondre strictement à la spécification ODT 1.1. OOo 3.0 affiche correctement les fichiers lorsqu'ils contiennent des éléments et des attributs d'ODT 1.2. Utilisez « false » à cette fin, ou « true » pour une conformité stricte à la spécification 1.1. La valeur par défaut est`FAUX` . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit/) { get; set; } | Permet de spécifier les unités de mesure à appliquer au contenu du document. La valeur par défaut estCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Obtient ou définit une valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est`FAUX` . |
| [Password](../../aspose.words.saving/odtsaveoptions/password/) { get; set; } | Obtient ou définit un mot de passe pour crypter le document. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quand`vrai` , joli format de sortie le cas échéant. La valeur par défaut est`FAUX` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Appelé lors de l'enregistrement d'un document et accepte les données sur la progression de l'enregistrement. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat/) { get; set; } | Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut êtreOdt ouOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Spécifie le dossier pour les fichiers temporaires utilisés lors de l'enregistrement dans un fichier DOC ou DOCX. Par défaut, cette propriété est`nul` et aucun fichier temporaire n'est utilisé. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Détermine si les attributs de police seront modifiés en fonction du code de caractère utilisé. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la propriété est mise à jour avant l'enregistrement. La valeur par défaut est`FAUX` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Obtient ou définit une valeur déterminant si les champs de certains types doivent être mis à jour avant d'enregistrer le document dans un format de page fixe. La valeur par défaut de cette propriété est`vrai` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la propriété est mise à jour avant l'enregistrement. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Obtient ou définit une valeur déterminant si le[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la propriété est mise à jour avant l'enregistrement. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser l'anticrénelage pour le rendu. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Obtient ou définit une valeur déterminant s'il faut ou non utiliser des algorithmes de rendu de haute qualité (c'est-à-dire lents). |

## Remarques

Pour le moment, il ne fournit que le[`SaveFormat`](./saveformat/) propriété, mais à l'avenir, d'autres options seront ajoutées, telles qu'un mot de passe de cryptage ou des paramètres de signature numérique.

## Exemples

Montre comment rendre un document enregistré conforme à un ancien schéma ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Montre comment utiliser différentes unités de mesure pour définir les paramètres de style d'un document ODT enregistré.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Lorsque nous exportons le document vers .odt, nous pouvons utiliser un objet OdtSaveOptions pour modifier la façon dont nous enregistrons le document.
// Nous pouvons définir la propriété « MeasureUnit » sur « OdtSaveMeasureUnit.Centimeters »
 // pour définir du contenu tel que des paramètres de style à l'aide du système métrique, utilisé par Open Office.
// Nous pouvons définir la propriété « MeasureUnit » sur « OdtSaveMeasureUnit.Inches »
// pour définir du contenu tel que des paramètres de style à l'aide du système impérial, utilisé par Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Voir également

* class [SaveOptions](../saveoptions/)
* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
