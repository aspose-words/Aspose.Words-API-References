---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: .NET için Aspose.Words
description: ImageWatermarkOptions'ın IsWashout özelliğini keşfedin. Bu basit boolean ayarıyla filigranınızın washout efektini zahmetsizce kontrol edin.
type: docs
weight: 20
url: /tr/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Filigranın silinme etkisinden sorumlu olan bir Boole değeri alır veya ayarlar. Varsayılan değer`doğru` .

```csharp
public bool IsWashout { get; set; }
```

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
