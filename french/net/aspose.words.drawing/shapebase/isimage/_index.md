---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words pour .NET
description: Découvrez si une forme est une image grâce à la propriété IsImage de ShapeBase. Identifiez facilement les formes d'image pour une flexibilité et des fonctionnalités de conception améliorées.
type: docs
weight: 300
url: /fr/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

Retours`vrai` si cette forme est une forme d'image.

```csharp
public bool IsImage { get; }
```

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

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
