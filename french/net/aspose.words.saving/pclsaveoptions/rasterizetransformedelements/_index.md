---
title: PclSaveOptions.RasterizeTransformedElements
second_title: Référence de l'API Aspose.Words pour .NET
description: PclSaveOptions propriété. Obtient ou définit une valeur déterminant si les éléments transformés complexes doivent être rastérisés avant dêtre enregistrés dans un document PCL. La valeur par défaut estvrai .
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Obtient ou définit une valeur déterminant si les éléments transformés complexes doivent être rastérisés avant d'être enregistrés dans un document PCL. La valeur par défaut est`vrai` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

### Remarques

PCL ne prend pas en charge certains types de transformations utilisées par Aspose Words. Par exemple, les images pivotées et inclinées et les pinceaux de texture. Pour rendre correctement ces éléments, le processus de rastérisation est utilisé, c'est-à-dire l'enregistrement dans l'image et le découpage. Ce processus peut prendre du temps et de la mémoire supplémentaires. Si l'indicateur est défini sur`FAUX` , certains contenus de la sortie peuvent être différents par rapport au document source.

### Exemples

Montre comment rastériser des éléments complexes lors de l’enregistrement d’un document au format PCL.

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
* espace de noms [Aspose.Words.Saving](../../pclsaveoptions/)
* Assemblée [Aspose.Words](../../../)


