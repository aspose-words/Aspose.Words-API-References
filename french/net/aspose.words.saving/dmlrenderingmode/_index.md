---
title: Enum DmlRenderingMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.DmlRenderingMode énumération. Spécifie comment les formes DrawingML sont rendues aux formats de page fixes.
type: docs
weight: 4660
url: /fr/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

Spécifie comment les formes DrawingML sont rendues aux formats de page fixes.

```csharp
public enum DmlRenderingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Fallback | `0` | Si la forme de repli est disponible pour DrawingML, Aspose.Words rend la forme de repli au lieu de DrawingML. |
| DrawingML | `1` | Aspose.Words ignore la forme de secours de DrawingML et rend DrawingML lui-même. Il s'agit du mode par défaut. |

### Exemples

Montre comment rendre les formes de secours lors de l'enregistrement au format PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "DmlRenderingMode" sur "DmlRenderingMode.Fallback"
// pour remplacer les formes DML par leurs formes de secours.
// Définissez la propriété "DmlRenderingMode" sur "DmlRenderingMode.DrawingML"
// pour restituer les formes DML elles-mêmes.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Montre comment configurer la qualité de rendu des effets DrawingML dans un document lorsque nous l'enregistrons au format PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.None" pour supprimer tous les effets DrawingML.
// Définissez la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.Simplified"
// pour rendre une version simplifiée des effets DrawingML.
// Définissez la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.Fine" pour
// Rendre les effets DrawingML avec plus de précision et aussi avec plus de coût de traitement.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


