---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SaveOptions ImlRenderingMode améliore le rendu des objets InkML. Optimisez votre rendu Ink pour de meilleurs résultats visuels !
type: docs
weight: 90
url: /fr/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Obtient ou définit une valeur déterminant la manière dont les objets d'encre (InkML) sont rendus.

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Remarques

La valeur par défaut estInkML .

Cette propriété est utilisée lorsque le document est exporté vers des formats de page fixes.

## Exemples

Montre comment rendre l'objet Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// L'ensemble « ImlRenderingMode.InkML » ignore la forme de secours de l'objet Ink (InkML) et restitue InkML lui-même.
// Si le résultat du rendu n'est pas satisfaisant,
// veuillez utiliser 'ImlRenderingMode.Fallback' pour obtenir un résultat similaire aux versions précédentes.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Voir également

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
