---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words ImlRenderingMode pour un rendu InkML optimal. Améliorez la qualité de vos documents grâce à une visualisation précise des objets d'encre !
type: docs
weight: 6000
url: /fr/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Spécifie comment les objets d'encre (InkML) sont rendus dans des formats de page fixes.

```csharp
public enum ImlRenderingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Fallback | `0` | Si la forme de secours est disponible pour l'objet Ink (InkML), Aspose.Words restitue la forme de secours au lieu de l'objet InkML. |
| InkML | `1` | Aspose.Words ignore la forme de secours de l'objet Ink (InkML) et restitue InkML lui-même. Il s'agit du mode par défaut. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
