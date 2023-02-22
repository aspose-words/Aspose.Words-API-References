---
title: DownsampleOptions.Resolution
second_title: Référence de l'API Aspose.Words pour .NET
description: DownsampleOptions propriété. Spécifie la résolution en pixels par pouce à laquelle les images doivent être souséchantillonnées.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Spécifie la résolution en pixels par pouce à laquelle les images doivent être sous-échantillonnées.

```csharp
public int Resolution { get; set; }
```

### Remarques

La valeur par défaut est 220 ppi.

### Exemples

Montre comment modifier la résolution des images dans le document PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Par défaut, Aspose.Words sous-échantillonne toutes les images d'un document que nous enregistrons au format PDF à 220 ppi.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Définissez la propriété "Résolution" sur "36" pour sous-échantillonner toutes les images à 36 ppi.
options.DownsampleOptions.Resolution = 36;

// Définissez la propriété "ResolutionThreshold" pour n'appliquer le sous-échantillonnage qu'à
// images avec une résolution supérieure à 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// Seules les deux premières images du document seront sous-échantillonnées à ce stade.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Voir également

* class [DownsampleOptions](../)
* espace de noms [Aspose.Words.Saving](../../downsampleoptions/)
* Assemblée [Aspose.Words](../../../)


