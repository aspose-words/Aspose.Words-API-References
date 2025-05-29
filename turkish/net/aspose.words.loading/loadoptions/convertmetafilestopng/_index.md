---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: .NET için Aspose.Words
description: WMF ve EMF meta dosyalarını LoadOptions ile zahmetsizce PNG formatına dönüştürün. Görüntü yönetiminizi basitleştirin ve uyumluluğu bugün artırın!
type: docs
weight: 30
url: /tr/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Meta dosyasının dönüştürülüp dönüştürülmeyeceğini alır veya ayarlarWmf veyaEmf ) görüntüleriPnggörüntü biçimi.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## Notlar

Meta dosyaları (Wmf veyaEmf ) sıkıştırılmamış bir görüntü biçimidir ve bazen belgeyi tutmak ve işlemek için çok fazla RAM gerektirir. Bu seçenek tüm meta dosyası görüntülerini dönüştürmeye olanak tanırPng Belge yüklenirken. Lütfen dikkat - vektörel grafikleri raster'a dönüştürmek görüntülerin kalitesini düşürür.

## Örnekler

Belge yüklenirken WMF/EMF'nin PNG'ye nasıl dönüştürüleceğini gösterir.

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

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
