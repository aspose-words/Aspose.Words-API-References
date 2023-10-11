---
title: ImageData.ImageBytes
second_title: Référence de l'API Aspose.Words pour .NET
description: ImageData propriété. Obtient ou définit les octets bruts de limage stockée dans la forme.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Obtient ou définit les octets bruts de l'image stockée dans la forme.

```csharp
public byte[] ImageBytes { get; set; }
```

### Remarques

Définir la valeur sur`nul` ou un tableau vide supprimera l'image de la forme.

Retour`nul` si l'image n'est pas stockée dans le document (par exemple l'image est probablement liée dans ce cas).

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


