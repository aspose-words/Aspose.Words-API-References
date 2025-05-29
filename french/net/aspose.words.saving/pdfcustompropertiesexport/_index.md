---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words pour .NET
description: Découvrez comment l'énumération Aspose.Words.PdfCustomPropertiesExport améliore les exportations PDF en personnalisant les propriétés du document pour des résultats optimaux.
type: docs
weight: 6210
url: /fr/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Spécifie la manière[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) sont exportés vers un fichier PDF.

```csharp
public enum PdfCustomPropertiesExport
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucune propriété personnalisée n'est exportée. |
| Standard | `1` | Les propriétés personnalisées sont exportées sous forme d'entrées dans le dictionnaire /Info. |
| Metadata | `2` | Les propriétés personnalisées sont des métadonnées. |

## Exemples

Montre comment exporter des propriétés personnalisées lors de la conversion d'un document au format PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « CustomPropertiesExport » sur « PdfCustomPropertiesExport.None » pour la supprimer
// propriétés de document personnalisées lorsque nous enregistrons le document au format .PDF.
// Définissez la propriété « CustomPropertiesExport » sur « PdfCustomPropertiesExport.Standard »
// pour conserver les propriétés personnalisées dans le document PDF de sortie.
// Définissez la propriété « CustomPropertiesExport » sur « PdfCustomPropertiesExport.Metadata »
// pour conserver les propriétés personnalisées dans un paquet XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
