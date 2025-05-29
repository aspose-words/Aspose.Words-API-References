---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: .NET için Aspose.Words
description: Aspose.Words.ImageWatermarkOptions'ı keşfedin. Gelişmiş belge sunumu için çok yönlü seçeneklerle görüntü filigranlarınızı zahmetsizce özelleştirin.
type: docs
weight: 3670
url: /tr/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

Resimle filigran eklerken belirtilebilecek seçenekleri içerir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Filigranla Çalışma](https://docs.aspose.com/words/net/working-with-watermark/) belgeleme makalesi.

```csharp
public class ImageWatermarkOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | Filigranın silinme etkisinden sorumlu olan bir Boole değeri alır veya ayarlar. Varsayılan değer`doğru` . |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | Görüntünün bir kesri olarak ifade edilen ölçek faktörünü alır veya ayarlar. Varsayılan değer 0'dır - auto. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
