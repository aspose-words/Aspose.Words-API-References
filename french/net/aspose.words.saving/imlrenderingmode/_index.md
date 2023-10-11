---
title: Enum ImlRenderingMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Saving.ImlRenderingMode énumération. Spécifie comment les objets Ink InkML sont rendus dans des formats de page fixes.
type: docs
weight: 5250
url: /fr/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Spécifie comment les objets Ink (InkML) sont rendus dans des formats de page fixes.

```csharp
public enum ImlRenderingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Fallback | `0` | Si une forme de secours est disponible pour l'objet Ink (InkML), Aspose.Words restitue la forme de secours au lieu de InkML. |
| InkML | `1` | Aspose.Words ignore la forme de repli de l'objet Ink (InkML) et restitue InkML lui-même. Il s'agit du mode par défaut. |

### Exemples

Montre comment restituer un objet Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Définir 'ImlRenderingMode.InkML' ignore la forme de repli de l'objet Ink (InkML) et restitue InkML lui-même.
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


