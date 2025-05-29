---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PdfSaveOptions UseBookFoldPrintingSettings pour enregistrer facilement des documents dans une mise en page de livret pour une efficacité d'impression améliorée.
type: docs
weight: 320
url: /fr/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré à l'aide d'une mise en page d'impression de livret, si elle est spécifiée via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Remarques

Si cette option est spécifiée,[`PageSet`](../../fixedpagesaveoptions/pageset/) est ignoré lors de l'enregistrement. Ce comportement correspond à MS Word. Si les paramètres d'impression de pliage de livre ne sont pas spécifiés dans la mise en page, cette option n'aura aucun effet.

## Exemples

Montre comment enregistrer un document au format PDF sous la forme d'un livre plié.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « UseBookFoldPrintingSettings » sur « true » pour organiser le contenu
// dans le PDF de sortie d'une manière qui nous aide à l'utiliser pour créer un livret.
// Définissez la propriété « UseBookFoldPrintingSettings » sur « false » pour restituer le PDF normalement.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Si nous rendons le document sous forme de livret, nous devons définir les « MultiplePages »
// propriétés des objets de mise en page de toutes les sections sur « MultiplePagesType.BookFoldPrinting ».
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Une fois que nous aurons imprimé ce document sur les deux côtés des pages, nous pourrons plier toutes les pages au milieu en même temps,
// et le contenu s'alignera de manière à créer un livret.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
