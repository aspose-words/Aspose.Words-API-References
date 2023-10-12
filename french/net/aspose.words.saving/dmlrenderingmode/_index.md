---
title: Enum DmlRenderingMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.DmlRenderingMode énumération. Spécifie comment les formes DrawingML sont rendues dans des formats de page fixes.
type: docs
weight: 4920
url: /fr/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

Spécifie comment les formes DrawingML sont rendues dans des formats de page fixes.

```csharp
public enum DmlRenderingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Fallback | `0` | Si la forme de secours est disponible pour DrawingML, Aspose.Words affiche la forme de secours au lieu de DrawingML. |
| DrawingML | `1` | Aspose.Words ignore la forme de secours de DrawingML et restitue DrawingML lui-même. Il s'agit du mode par défaut. |

### Exemples

Montre comment restituer des formes de secours lors de l’enregistrement au format PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définit la propriété "DmlRenderingMode" sur "DmlRenderingMode.Fallback"
// pour remplacer les formes DML par leurs formes de secours.
// Définit la propriété "DmlRenderingMode" sur "DmlRenderingMode.DrawingML"
// pour restituer les formes DML elles-mêmes.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Montre comment configurer la qualité de rendu des effets DrawingML dans un document lorsque nous l'enregistrons au format PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.None" pour supprimer tous les effets DrawingML.
// Définit la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.Simplified"
// pour afficher une version simplifiée des effets DrawingML.
// Définissez la propriété "DmlEffectsRenderingMode" sur "DmlEffectsRenderingMode.Fine" pour
// rend les effets DrawingML avec plus de précision et également avec un coût de traitement plus élevé.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)


