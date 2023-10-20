---
title: PdfSaveOptions.DownsampleOptions
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words pour .NET
description: PdfSaveOptions DownsampleOptions propriété. Permet de spécifier les options de souséchantillonnage en C#.
type: docs
weight: 100
url: /fr/net/aspose.words.saving/pdfsaveoptions/downsampleoptions/
---
## PdfSaveOptions.DownsampleOptions property

Permet de spécifier les options de sous-échantillonnage.

```csharp
public DownsampleOptions DownsampleOptions { get; set; }
```

## Exemples

Montre comment modifier la résolution des images dans le document PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Par défaut, Aspose.Words sous-échantillonne toutes les images d'un document que nous enregistrons au format PDF à 220 ppp.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Définissez la propriété "Résolution" sur "36" pour sous-échantillonner toutes les images à 36 ppp.
options.DownsampleOptions.Resolution = 36;

// Définissez la propriété "ResolutionThreshold" pour appliquer uniquement le sous-échantillonnage à
// images avec une résolution supérieure à 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// Seules les deux premières images du document seront sous-échantillonnées à ce stade.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Voir également

* class [DownsampleOptions](../../downsampleoptions/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
