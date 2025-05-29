---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: .NET için Aspose.Words
description: En iyi filigranlama için görüntü ölçeklemesini kolayca ayarlamak üzere ImageWatermarkOptions Scale özelliğini keşfedin. Sorunsuz entegrasyon için varsayılan değer 0 otomatiktir.
type: docs
weight: 30
url: /tr/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Görüntünün bir kesri olarak ifade edilen ölçek faktörünü alır veya ayarlar. Varsayılan değer 0'dır - auto.

```csharp
public double Scale { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Argüman geçerli değerler aralığının dışında olduğunda fırlatılır. |

## Notlar

Geçerli değerler 0 ile 65,5 arasındadır.

Otomatik ölçekleme, filigranın sayfa kenar boşluklarına göre maksimum genişliğine ve maksimum yüksekliğine ölçekleneceği anlamına gelir.

## Örnekler

Yerel dosya sistemindeki bir görüntüden filigranın nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

            // Resim filigranının görünümünü ImageWatermarkOptions nesnesiyle değiştirin,
            // daha sonra bir resim dosyasından filigran oluştururken bunu geçirin.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Resim eklemek için farklı seçeneklerimiz var:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ayrıca bakınız

* class [ImageWatermarkOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
