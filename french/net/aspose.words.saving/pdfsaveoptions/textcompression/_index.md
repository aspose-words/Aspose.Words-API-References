---
title: PdfSaveOptions.TextCompression
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Spécifie le type de compression à utiliser pour tout le contenu textuel du document.
type: docs
weight: 290
url: /fr/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Spécifie le type de compression à utiliser pour tout le contenu textuel du document.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

### Remarques

La valeur par défaut estFlate.

Augmente considérablement la taille de sortie lors de l'enregistrement d'un document sans compression.

### Exemples

Montre comment appliquer une compression de texte lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définit la propriété "TextCompression" sur "PdfTextCompression.None" pour n'appliquer aucune
// compression en texte lorsque nous enregistrons le document au format PDF.
// Définissez la propriété "TextCompression" sur "PdfTextCompression.Flate" pour appliquer la compression ZIP
// en texte lorsque nous enregistrons le document au format PDF. Plus le document est volumineux, plus l’impact qu’il aura sera important.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Voir également

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


