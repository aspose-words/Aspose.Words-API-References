---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété UseEmfEmbeddedToWmf optimise le rendu des métafichiers WMF, améliorant ainsi les performances et la qualité de vos applications graphiques.
type: docs
weight: 70
url: /fr/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Obtient ou définit une valeur déterminant comment les métafichiers WMF avec des métafichiers EMF intégrés doivent être rendus.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Remarques

Les métafichiers WMF peuvent contenir des données EMF intégrées. MS Word utilise généralement des données EMF intégrées. GDI+ utilise toujours des données WMF.

Lorsque cette valeur est définie sur`vrai`Aspose.Words utilise des données EMF intégrées lors du rendu.

Lorsque cette valeur est définie sur`FAUX`Aspose.Words utilise les données WMF lors du rendu.

Cette option est utilisée uniquement lorsque le métafichier est rendu au format vectoriel. Lorsque le métafichier est rendu au format bitmap, les données WMF sont toujours utilisées.

La valeur par défaut est`vrai`.

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

* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
