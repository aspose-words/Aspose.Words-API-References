---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: Aspose.Words pour .NET
description: Contrôlez la structure d'exportation de vos documents avec PdfSaveOptions. Gérez facilement les paramètres pour une sortie PDF optimale et optimisez votre flux de travail.
type: docs
weight: 140
url: /fr/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Obtient ou définit une valeur déterminant s'il faut ou non exporter la structure du document.

```csharp
public bool ExportDocumentStructure { get; set; }
```

## Remarques

Cette valeur est ignorée lors de l'enregistrement au format PDF/A-1a, PDF/A-2a et PDF/UA-1 car la structure du document est requise pour cette conformité.

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les documents volumineux.

## Exemples

Montre comment préserver les éléments de structure du document, ce qui peut aider à interpréter par programmation notre document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Définissez la propriété « ExportDocumentStructure » sur « true » pour rendre la structure du document, comme les balises, disponibles via le
// Volet de navigation « Contenu » d'Adobe Acrobat au prix d'une augmentation de la taille du fichier.
// Définissez la propriété « ExportDocumentStructure » sur « false » pour ne pas exporter la structure du document.
options.ExportDocumentStructure = exportDocumentStructure;

// Supposons que nous exportions la structure du document lors de son enregistrement. Dans ce cas,
// nous pouvons l'ouvrir en utilisant Adobe Acrobat et trouver des balises pour des éléments tels que le titre
// et le paragraphe suivant via "Affichage" -> "Afficher/Masquer" -> "Volets de navigation" -> "Tags".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
