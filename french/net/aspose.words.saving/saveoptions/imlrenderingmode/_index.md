---
title: SaveOptions.ImlRenderingMode
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Obtient ou définit une valeur déterminant la manière dont les objets Ink InkML sont rendus.
type: docs
weight: 90
url: /fr/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Obtient ou définit une valeur déterminant la manière dont les objets Ink (InkML) sont rendus.

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

### Remarques

La valeur par défaut estInkML .

Cette propriété est utilisée lorsque le document est exporté vers des formats de page fixes.

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

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


