---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété RtfSaveOptions SaveImagesAsWmf améliore votre document en enregistrant toutes les images au format WMF pour une qualité et une compatibilité supérieures.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

Quand`vrai` toutes les images seront enregistrées au format WMF.

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## Remarques

Cette option peut aider à éviter les messages d'avertissement de WordPad.

## Exemples

Montre comment convertir toutes les images d'un document au format Windows Metafile lorsque nous enregistrons le document au format RTF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg");

Assert.AreEqual(ImageType.Jpeg, imageShape.ImageData.ImageType);

builder.InsertParagraph();
builder.Writeln("Png image:");
imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ImageType.Png, imageShape.ImageData.ImageType);

// Créez un objet « RtfSaveOptions » à transmettre à la méthode « Save » du document pour modifier la façon dont nous l'enregistrons dans un RTF.
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// Définissez la propriété « SaveImagesAsWmf » sur « true » pour convertir toutes les images du document en WMF lorsque nous l'enregistrons en RTF.
// Cela aidera les lecteurs tels que WordPad à lire notre document.
// Définissez la propriété « SaveImagesAsWmf » sur « false » pour conserver le format d'origine de toutes les images du document
// lors de l'enregistrement au format RTF. Cela préservera la qualité des images au détriment de la compatibilité avec les anciens lecteurs RTF.
rtfSaveOptions.SaveImagesAsWmf = saveImagesAsWmf;

doc.Save(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = new Document(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf");

NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

if (saveImagesAsWmf)
{
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[1]).ImageData.ImageType);
}
else
{
    Assert.AreEqual(ImageType.Jpeg, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Png, ((Shape)shapes[1]).ImageData.ImageType);
}
```

### Voir également

* class [RtfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
