---
title: PdfSaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PdfSaveOptions DmlEffectsRenderingMode pour contrôler le rendu des effets DrawingML pour une qualité de sortie PDF améliorée.
type: docs
weight: 100
url: /fr/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

Obtient ou définit une valeur déterminant comment les effets DrawingML sont rendus.

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Remarques

La valeur par défaut estSimplified .

Cette propriété est utilisée lorsque le document est exporté vers des formats de page fixes.

Si[`Compliance`](../compliance/) est réglé surPdfA1a ouPdfA1b La propriété , renvoie toujoursNone.

## Exemples

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
