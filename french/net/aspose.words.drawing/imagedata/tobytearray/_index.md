---
title: ImageData.ToByteArray
second_title: Référence de l'API Aspose.Words pour .NET
description: ImageData méthode. Renvoie les octets dimage pour nimporte quelle image que limage soit stockée ou liée.
type: docs
weight: 220
url: /fr/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Renvoie les octets d'image pour n'importe quelle image, que l'image soit stockée ou liée.

```csharp
public byte[] ToByteArray()
```

### Remarques

Si l'image est liée, télécharge l'image à chaque appel.

### Exemples

Montre comment créer un fichier image à partir des données d’image brutes d’une forme.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() renvoie le tableau stocké dans la propriété ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Enregistrez les données d'image de la forme dans un fichier image dans le système de fichiers local.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### Voir également

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../imagedata/)
* Assemblée [Aspose.Words](../../../)


