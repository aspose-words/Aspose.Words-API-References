---
title: PdfSaveOptions.CustomPropertiesExport
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Obtient ou définit une valeur déterminant la manièreCustomDocumentProperties sont exportés vers un fichier PDF.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

Obtient ou définit une valeur déterminant la manière[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) sont exportés vers un fichier PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

### Remarques

La valeur par défaut estNone.

Metadata la valeur n'est pas prise en charge lors de l'enregistrement au format PDF/A. Standard sera utilisé à la place pour PDF/A-1 et PDF/A-2 et None pour PDF/A-4.

Standard la valeur n'est pas prise en charge lors de l'enregistrement au format PDF 2.0. Metadata sera utilisé à la place.

### Exemples

Montre comment exporter des propriétés personnalisées lors de la conversion d'un document au format PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "CustomPropertiesExport" sur "PdfCustomPropertiesExport.None" pour la supprimer
// Propriétés personnalisées du document lorsque nous enregistrons le document au format .PDF.
// Définit la propriété "CustomPropertiesExport" sur "PdfCustomPropertiesExport.Standard"
// pour conserver les propriétés personnalisées dans le document PDF de sortie.
// Définissez la propriété "CustomPropertiesExport" sur "PdfCustomPropertiesExport.Metadata"
// pour conserver les propriétés personnalisées dans un paquet XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### Voir également

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


