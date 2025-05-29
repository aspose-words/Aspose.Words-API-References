---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HtmlLoadOptions SupportVml améliore votre expérience Web en activant la prise en charge des images VML pour une qualité graphique améliorée.
type: docs
weight: 70
url: /fr/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

Obtient ou définit une valeur indiquant s'il faut prendre en charge les images VML.

```csharp
public bool SupportVml { get; set; }
```

## Exemples

Montre comment prendre en charge les commentaires conditionnels lors du chargement d'un document HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Si la valeur est vraie, nous prenons en compte le code VML lors de l'analyse du document chargé.
loadOptions.SupportVml = supportVml;

// Ce document contient une image JPEG dans les balises « <!--[if gte vml 1]> »,
// et une image PNG différente dans les balises "<![if !vml]>".
// Si nous définissons l'indicateur « SupportVml » sur « true », alors Aspose.Words chargera le JPEG.
// Si nous définissons cet indicateur sur « false », alors Aspose.Words chargera uniquement le PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Voir également

* class [HtmlLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
