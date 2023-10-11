---
title: PdfSaveOptions.ExportDocumentStructure
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Obtient ou définit une valeur déterminant sil faut ou non exporter la structure du document.
type: docs
weight: 140
url: /fr/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Obtient ou définit une valeur déterminant s'il faut ou non exporter la structure du document.

```csharp
public bool ExportDocumentStructure { get; set; }
```

### Remarques

Cette valeur est ignorée lors de l'enregistrement au format PDF/A-1a, PDF/A-2a et PDF/UA-1 car la structure du document est requise pour cette conformité.

Notez que l'exportation de la structure du document augmente considérablement la consommation de mémoire, en particulier pour les documents volumineux.

### Exemples

Montre comment préserver les éléments de structure du document, qui peuvent aider à interpréter notre document par programmation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "ExportDocumentStructure" sur "true" pour rendre la structure du document, telles que les balises, disponible via le
// Volet de navigation "Contenu" d'Adobe Acrobat au prix d'une taille de fichier accrue.
// Définissez la propriété "ExportDocumentStructure" sur "false" pour ne pas exporter la structure du document.
options.ExportDocumentStructure = exportDocumentStructure;

// Supposons que nous exportions la structure du document tout en enregistrant ce document. Dans ce cas,
// nous pouvons l'ouvrir avec Adobe Acrobat et trouver des balises pour des éléments tels que le titre
// et le paragraphe suivant via "View" -> "Afficher/Masquer" -> "Volets de navigation" -> "Mots clés".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


