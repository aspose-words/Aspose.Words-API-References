---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SaveFormat de PsSaveOptions pour spécifier facilement le format d'enregistrement de votre document. Optimisez votre flux de travail grâce à des options d'enregistrement flexibles !
type: docs
weight: 20
url: /fr/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtrePs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
