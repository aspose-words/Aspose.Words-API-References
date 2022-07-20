---
title: ImlRenderingMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit une valeur déterminant le rendu des objets dencre InkML.
type: docs
weight: 100
url: /fr/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Obtient ou définit une valeur déterminant le rendu des objets d'encre (InkML).

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

### Remarques

La valeur par défaut estInkML .

Cette propriété est utilisée lorsque le document est exporté vers des formats de page fixes.

### Exemples

Montre comment rendre l'objet Ink.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Set 'ImlRenderingMode.InkML' ignore la forme de repli de l'objet d'encre (InkML) et rend InkML lui-même.
// Si le résultat du rendu n'est pas satisfaisant,
// veuillez utiliser 'ImlRenderingMode.Fallback' pour obtenir un résultat similaire aux versions précédentes.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Voir également

* enum [ImlRenderingMode](../../imlrenderingmode)
* class [SaveOptions](../../saveoptions)
* espace de noms [Aspose.Words.Saving](../../saveoptions)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->