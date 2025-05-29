---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageData ImageBytes pour gérer et manipuler facilement les octets d'image bruts dans vos formes pour un contenu visuel amélioré.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Obtient ou définit les octets bruts de l'image stockée dans la forme.

```csharp
public byte[] ImageBytes { get; set; }
```

## Remarques

Définition de la valeur à`nul` ou un tableau vide supprimera l'image de la forme.

Retours`nul` si l'image n'est pas stockée dans le document (par exemple, l'image est probablement liée dans ce cas).

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
