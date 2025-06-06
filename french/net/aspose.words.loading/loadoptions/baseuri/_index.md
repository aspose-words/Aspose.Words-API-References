---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words pour .NET
description: Découvrez la propriété LoadOptions BaseUri pour convertir facilement les URI relatifs en URI absolus dans vos documents. Optimisez votre gestion des URI dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Obtient ou définit la chaîne qui sera utilisée pour résoudre les URI relatifs trouvés dans le document en URI absolus lorsque cela est nécessaire. Peut être`nul` ou chaîne vide. La valeur par défaut est`nul` .

```csharp
public string BaseUri { get; set; }
```

## Remarques

Cette propriété est utilisée pour résoudre les URI relatifs en absolus dans les cas suivants :

1. Lors du chargement d'un document HTML à partir d'un flux et que le document contient des images avec des URI relatifs et n'a pas d'URI de base spécifié dans l'élément HTML BASE.
2. Lors de l'enregistrement d'un document au format PDF et dans d'autres formats, pour récupérer les images liées à l'aide d'URI relatifs afin que les images puissent être enregistrées dans le document de sortie.

## Exemples

Montre comment ouvrir un document HTML avec des images d'un flux à l'aide d'un URI de base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Transmettez l'URI du dossier de base lors de son chargement
    // afin que toutes les images avec des URI relatives dans le document HTML puissent être trouvées.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Vérifiez que la première forme du document contient une image valide.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
