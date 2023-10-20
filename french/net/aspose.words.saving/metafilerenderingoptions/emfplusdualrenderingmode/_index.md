---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words pour .NET
description: MetafileRenderingOptions EmfPlusDualRenderingMode propriété. Obtient ou définit une valeur déterminant comment les métafichiers EMF Dual doivent être rendus en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

Obtient ou définit une valeur déterminant comment les métafichiers EMF+ Dual doivent être rendus.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## Remarques

Les métafichiers EMF+ Dual contiennent à la fois des parties EMF+ et EMF. MS Word et GDI+ restituent toujours la partie EMF+. Aspose.Words ne prend actuellement pas entièrement en charge tous les enregistrements EMF+ et, dans certains cas, le résultat du rendu de la partie EMF est meilleur que le résultat du rendu de la partie EMF+.

Cette option est utilisée uniquement lorsque le métafichier est rendu sous forme de graphiques vectoriels. Lorsque le métafichier est rendu en bitmap, la partie EMF+ est toujours utilisée.

La valeur par défaut estEmfPlusWithFallback.

## Exemples

Montre comment configurer les options de rendu liées aux métafichiers Windows améliorés lors de l’enregistrement au format PDF.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définit la propriété "EmfPlusDualRenderingMode" sur "EmfPlusDualRenderingMode.Emf"
// pour afficher uniquement la partie EMF d'un double métafichier EMF+.
// Définissez la propriété "EmfPlusDualRenderingMode" sur "EmfPlusDualRenderingMode.EmfPlus" pour
// pour restituer la partie EMF+ d'un double métafichier EMF+.
// Définit la propriété "EmfPlusDualRenderingMode" sur "EmfPlusDualRenderingMode.EmfPlusWithFallback"
// pour restituer la partie EMF+ d'un double métafichier EMF+ si tous les enregistrements EMF+ sont pris en charge.
// Sinon, Aspose.Words restituera la partie EMF.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Définissez la propriété "UseEmfEmbeddedToWmf" sur "true" pour restituer les données EMF intégrées
// pour les métafichiers que nous pouvons restituer sous forme de graphiques vectoriels.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Voir également

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
