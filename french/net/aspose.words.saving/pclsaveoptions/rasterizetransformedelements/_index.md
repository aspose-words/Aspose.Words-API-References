---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words pour .NET
description: Contrôlez la pixellisation des éléments complexes dans les documents PCL avec PclSaveOptions. Gérez facilement la qualité de l'image et la taille du fichier pour des résultats optimaux.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Obtient ou définit une valeur déterminant si les éléments transformés complexes doivent être pixellisés ou non avant d'être enregistrés dans un document PCL. La valeur par défaut est`vrai` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Remarques

PCL ne prend pas en charge certaines transformations utilisées par Aspose Words, par exemple les images pivotées, inclinées et les pinceaux de texture. Pour restituer correctement ces éléments, un processus de rastérisation est utilisé, c'est-à-dire l'enregistrement dans l'image et le découpage. Ce processus peut nécessiter du temps et de la mémoire supplémentaires. Si l'option est définie sur`FAUX` , certains contenus de sortie peuvent être différents par rapport au document source.

## Exemples

Montre comment pixelliser des éléments complexes lors de l'enregistrement d'un document au format PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Voir également

* class [PclSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
