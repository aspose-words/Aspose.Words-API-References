---
title: DownsampleOptions.ResolutionThreshold
linktitle: ResolutionThreshold
articleTitle: ResolutionThreshold
second_title: Aspose.Words pour .NET
description: Optimisez vos images avec la propriété « Seuil de résolution » de DownsampleOptions. Contrôlez le sous-échantillonnage en fonction de la résolution pour de meilleures performances et une meilleure qualité.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

Spécifie la résolution de seuil en pixels par pouce. Si la résolution d'une image dans le document est inférieure à la valeur de seuil, l'algorithme de sous-échantillonnage ne sera pas appliqué. Une valeur de 0 signifie que la vérification de seuil n'est pas utilisée et que toutes les images dont la taille peut être réduite sont sous-échantillonnées.

```csharp
public int ResolutionThreshold { get; set; }
```

## Remarques

La valeur par défaut est 0.

## Exemples

Montre comment modifier la résolution des images dans le document PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Par défaut, Aspose.Words sous-échantillonne toutes les images d'un document que nous enregistrons au format PDF à 220 ppp.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Définissez la propriété « Résolution » sur « 36 » pour sous-échantillonner toutes les images à 36 ppi.
options.DownsampleOptions.Resolution = 36;

// Définissez la propriété « ResolutionThreshold » pour appliquer uniquement le sous-échantillonnage à
// images avec une résolution supérieure à 128 ppp.
options.DownsampleOptions.ResolutionThreshold = 128;

// Seules les deux premières images du document seront sous-échantillonnées à ce stade.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Voir également

* class [DownsampleOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
