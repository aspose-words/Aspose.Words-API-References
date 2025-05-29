---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SaveOptions DmlRenderingMode améliore le rendu de vos formes DrawingML. Optimisez l'aspect visuel de vos documents sans effort !
type: docs
weight: 70
url: /fr/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

Obtient ou définit une valeur déterminant la manière dont les formes DrawingML sont rendues.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## Remarques

La valeur par défaut estFallback .

Cette propriété est utilisée lorsque le document est exporté vers des formats de page fixes.

## Exemples

Montre comment restituer des formes de secours lors de l'enregistrement au format PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « DmlRenderingMode » sur « DmlRenderingMode.Fallback »
// pour remplacer les formes DML par leurs formes de secours.
// Définissez la propriété « DmlRenderingMode » sur « DmlRenderingMode.DrawingML »
// pour restituer les formes DML elles-mêmes.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Montre comment configurer la qualité de rendu des effets DrawingML dans un document lorsque nous l'enregistrons au format PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « DmlEffectsRenderingMode » sur « DmlEffectsRenderingMode.None » pour supprimer tous les effets DrawingML.
// Définissez la propriété « DmlEffectsRenderingMode » sur « DmlEffectsRenderingMode.Simplified »
// pour rendre une version simplifiée des effets DrawingML.
// Définissez la propriété « DmlEffectsRenderingMode » sur « DmlEffectsRenderingMode.Fine » pour
// rendre les effets DrawingML avec plus de précision et également avec un coût de traitement plus élevé.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Voir également

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
