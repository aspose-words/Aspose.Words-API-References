---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words pour .NET
description: Optimisez vos exportations Markdown avec la propriété ImageResolution, qui permet de définir des résolutions de sortie personnalisées pour des images plus nettes. Par défaut : 96 ppp.
type: docs
weight: 60
url: /fr/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

Spécifie la résolution de sortie des images lors de l'exportation vers Markdown. La valeur par défaut est`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Exemples

Montre comment définir la résolution de sortie des images.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### Voir également

* class [MarkdownSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
