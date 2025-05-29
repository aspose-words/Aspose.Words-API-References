---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété PdfSaveOptions CustomPropertiesExport améliore vos exportations PDF en contrôlant CustomDocumentProperties pour des résultats optimaux.
type: docs
weight: 70
url: /fr/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Obtient ou définit une valeur déterminant la manière[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) sont exportés vers un fichier PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## Remarques

La valeur par défaut estNone.

Metadata la valeur n'est pas prise en charge lors de l'enregistrement au format PDF/A. Standard sera utilisé à la place pour PDF/A-1 et PDF/A-2 et None pour PDF/A-4.

Standard la valeur n'est pas prise en charge lors de l'enregistrement au format PDF 2.0. Metadata sera utilisé à la place.

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

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
