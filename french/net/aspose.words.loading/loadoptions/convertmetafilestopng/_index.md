---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words pour .NET
description: Convertissez facilement vos métafichiers WMF et EMF au format PNG avec LoadOptions. Simplifiez la gestion de vos images et améliorez la compatibilité dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Obtient ou définit s'il faut convertir le métafichier(Wmf ouEmf ) images àPngformat d'image.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## Remarques

Métafichiers (Wmf ouEmf ) est un format d'image non compressé et nécessite parfois trop de RAM pour contenir et traiter le document. Cette option permet de convertir toutes les images de métafichiers enPng lors du chargement du document. Attention : la conversion des graphiques vectoriels en raster diminue la qualité des images.

## Exemples

Montre comment convertir WMF/EMF en PNG lors du chargement du document.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.CreateImageDirectly.docx");

shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

TestUtil.VerifyImageInShape(1600, 1600, ImageType.Wmf, shape);

LoadOptions loadOptions = new LoadOptions();
loadOptions.ConvertMetafilesToPng = true;

doc = new Document(ArtifactsDir + "Image.CreateImageDirectly.docx", loadOptions);
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
