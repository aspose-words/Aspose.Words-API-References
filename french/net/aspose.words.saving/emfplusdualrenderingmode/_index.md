---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words pour .NET
description: Découvrez le mode de rendu double EMF Plus d'Aspose.Words pour un rendu optimal des métafichiers EMF Dual. Améliorez le traitement de vos documents avec précision !
type: docs
weight: 5730
url: /fr/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

Spécifie comment Aspose.Words doit restituer les métafichiers EMF+ Dual.

```csharp
public enum EmfPlusDualRenderingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words tente de restituer EMF+ dans le métafichier EMF+ Dual. Si certains enregistrements EMF+ ne sont pas pris en charge, Aspose.Words restitue EMF dans le métafichier EMF+ Dual. |
| EmfPlus | `1` | Aspose.Words rend EMF+ une partie du métafichier EMF+ Dual. |
| Emf | `2` | Aspose.Words rend EMF partie du métafichier EMF+ Dual. |

## Exemples

Montre comment configurer les options de rendu liées au métafichier Windows amélioré lors de l'enregistrement au format PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété « EmfPlusDualRenderingMode » sur « EmfPlusDualRenderingMode.Emf »
// pour restituer uniquement la partie EMF d'un métafichier double EMF+.
// Définissez la propriété « EmfPlusDualRenderingMode » sur « EmfPlusDualRenderingMode.EmfPlus » pour
// pour rendre la partie EMF+ d'un métafichier double EMF+.
// Définissez la propriété « EmfPlusDualRenderingMode » sur « EmfPlusDualRenderingMode.EmfPlusWithFallback »
// pour restituer la partie EMF+ d'un métafichier double EMF+ si tous les enregistrements EMF+ sont pris en charge.
// Sinon, Aspose.Words rendra la partie EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Définissez la propriété « UseEmfEmbeddedToWmf » sur « true » pour restituer les données EMF intégrées
// pour les métafichiers que nous pouvons restituer sous forme de graphiques vectoriels.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
