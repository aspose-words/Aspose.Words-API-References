---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: Aspose.Words pour .NET
description: MetafileRenderingOptions UseEmfEmbeddedToWmf propriété. Obtient ou définit une valeur déterminant comment les métafichiers WMF avec des métafichiers EMF intégrés doivent être rendus en C#.
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

Les métafichiers WMF peuvent contenir des données EMF intégrées. MS Word utilise dans la plupart des cas des données EMF intégrées. GDI+ utilise toujours des données WMF.

Lorsque cette valeur est fixée à`vrai`, Aspose.Words utilise les données EMF intégrées lors du rendu.

Lorsque cette valeur est fixée à`FAUX`, Aspose.Words utilise les données WMF lors du rendu.

Cette option est utilisée uniquement lorsque le métafichier est rendu sous forme de graphiques vectoriels. Lorsque le métafichier est rendu en bitmap, les données WMF sont toujours utilisées.

La valeur par défaut est`vrai`.

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

* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
