---
title: LoadOptions.ConvertMetafilesToPng
second_title: Référence de l'API Aspose.Words pour .NET
description: LoadOptions propriété. Obtient ou définit sil faut convertir le métafichier Wmf ouEmf  images àPng format dimage.
type: docs
weight: 30
url: /fr/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Obtient ou définit s'il faut convertir le métafichier (Wmf ouEmf ) images àPng format d'image.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

### Remarques

Métafichiers (Wmf ouEmf ) est un format d'image non compressé et nécessite parfois trop de RAM pour contenir et traiter le document. Cette option permet de convertir toutes les images de métafichier enPng lors du chargement du document. Veuillez noter que la conversion des graphiques vectoriels en raster diminue la qualité des images.

### Exemples

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

#if NET48
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#elif NET5_0_OR_GREATER
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#endif
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../loadoptions/)
* Assemblée [Aspose.Words](../../../)


