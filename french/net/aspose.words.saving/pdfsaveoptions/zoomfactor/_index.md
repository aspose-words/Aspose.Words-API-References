---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words pour .NET
description: PdfSaveOptions ZoomFactor propriété. Obtient ou définit une valeur déterminant le facteur de zoom en pourcentages pour un document en C#.
type: docs
weight: 330
url: /fr/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Obtient ou définit une valeur déterminant le facteur de zoom (en pourcentages) pour un document.

```csharp
public int ZoomFactor { get; set; }
```

## Remarques

Cette valeur est utilisée uniquement si[`ZoomBehavior`](../zoombehavior/) est réglé surZoomFactor .

## Exemples

Montre comment définir le zoom par défaut qu'un lecteur applique lors de l'ouverture d'un document PDF rendu.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
// Définissez la propriété "ZoomBehavior" sur "PdfZoomBehavior.ZoomFactor" pour qu'un lecteur PDF
// applique un facteur de zoom basé sur un pourcentage lorsque nous ouvrons le document avec.
// Fixez la propriété "ZoomFactor" à "25" pour donner au facteur de zoom une valeur de 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Lorsque nous ouvrons ce document à l'aide d'un lecteur tel qu'Adobe Acrobat, nous verrons le document mis à l'échelle à 1/4 de sa taille réelle.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
