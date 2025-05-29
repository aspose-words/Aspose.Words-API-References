---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PsSaveOptions UseBookFoldPrintingSettings pour enregistrer facilement des documents dans une mise en page de livret pour une efficacité d'impression améliorée.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Obtient ou définit une valeur booléenne indiquant si le document doit être enregistré à l'aide d'une mise en page d'impression de livret, si elle est spécifiée via[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Remarques

Si cette option est spécifiée,[`PageSet`](../../fixedpagesaveoptions/pageset/) est ignoré lors de l'enregistrement. Ce comportement correspond à MS Word. Si les paramètres d'impression de pliage de livre ne sont pas spécifiés dans la mise en page, cette option n'aura aucun effet.

## Exemples

Montre comment enregistrer un document au format Postscript sous la forme d'un pli de livre.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Créez un objet « PsSaveOptions » que nous pouvons transmettre à la méthode « Enregistrer » du document
// pour modifier la manière dont cette méthode convertit le document en PostScript.
// Définissez la propriété « UseBookFoldPrintingSettings » sur « true » pour organiser le contenu
// dans le document Postscript de sortie d'une manière qui nous aide à en faire un livret.
// Définissez la propriété « UseBookFoldPrintingSettings » sur « false » pour enregistrer le document normalement.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Si nous rendons le document sous forme de livret, nous devons définir les « MultiplePages »
// propriétés des objets de mise en page de toutes les sections sur « MultiplePagesType.BookFoldPrinting ».
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Une fois que nous aurons imprimé ce document sur les deux côtés des pages, nous pourrons plier toutes les pages au milieu en même temps,
// et le contenu s'alignera de manière à créer un livret.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Voir également

* class [PsSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
