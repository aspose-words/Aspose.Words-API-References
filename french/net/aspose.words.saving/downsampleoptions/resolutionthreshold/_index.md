---
title: DownsampleOptions.ResolutionThreshold
second_title: Référence de l'API Aspose.Words pour .NET
description: DownsampleOptions propriété. Spécifie la résolution du seuil en pixels par pouce. Si la résolution dune image dans le document est inférieure à la valeur seuil lalgorithme de souséchantillonnage ne sera pas appliqué. Une valeur de 0 signifie que la vérification du seuil nest pas utilisée et que toutes les images qui peuvent être réduits en taille sont souséchantillonnés.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/downsampleoptions/resolutionthreshold/
---
## DownsampleOptions.ResolutionThreshold property

Spécifie la résolution du seuil en pixels par pouce. Si la résolution d'une image dans le document est inférieure à la valeur seuil, l'algorithme de sous-échantillonnage ne sera pas appliqué. Une valeur de 0 signifie que la vérification du seuil n'est pas utilisée et que toutes les images qui peuvent être réduits en taille sont sous-échantillonnés.

```csharp
public int ResolutionThreshold { get; set; }
```

### Remarques

La valeur par défaut est 0.

### Exemples

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

* class [DownsampleOptions](../)
* espace de noms [Aspose.Words.Saving](../../downsampleoptions/)
* Assemblée [Aspose.Words](../../../)


