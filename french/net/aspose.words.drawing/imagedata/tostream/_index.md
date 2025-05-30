---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words pour .NET
description: Découvrez la méthode ImageData ToStream  convertissez efficacement les images en flux d'octets pour une gestion transparente des données et des performances d'application améliorées.
type: docs
weight: 240
url: /fr/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Crée et renvoie un flux contenant les octets de l'image.

```csharp
public Stream ToStream()
```

## Remarques

Si les octets de l'image sont stockés dans la forme, crée et renvoie unMemoryStream objet.

Si l'image est liée et stockée dans un fichier, ouvre le fichier et renvoie unFileStream objet.

Si l'image est liée et stockée dans une URL externe, télécharge le fichier et renvoie unMemoryStream objet.

Est-ce la responsabilité de l'appelant de supprimer l'objet de flux ?

## Exemples

Montre comment créer un fichier image à partir des données d'image brutes d'une forme.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() renvoie le tableau stocké dans la propriété ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Enregistrez les données d'image de la forme dans un fichier image du système de fichiers local.
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
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
