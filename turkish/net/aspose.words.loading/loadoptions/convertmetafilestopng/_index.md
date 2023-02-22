---
title: LoadOptions.ConvertMetafilesToPng
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Meta dosyasının Wmf veyaEmf  resimler içinPng resim formatı.
type: docs
weight: 30
url: /tr/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Meta dosyasının (Wmf veyaEmf ) resimler içinPng resim formatı.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

### Notlar

Meta dosyaları (Wmf veyaEmf ) sıkıştırılmamış bir görüntü biçimidir ve bazen belgeyi tutmak ve işlemek için çok fazla RAM gerektirir. Bu seçenek, tüm meta dosyası görüntülerininPng belge yüklemede. Lütfen dikkat - vektör grafiklerinin raster'e dönüştürülmesi görüntülerin kalitesini düşürür.

### Örnekler

Belge yükleme sırasında WMF/EMF'nin PNG'ye nasıl dönüştürüleceğini gösterir.

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

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


